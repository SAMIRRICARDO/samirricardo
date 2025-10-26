# AgilizaVRA — SaaS (Agenda, CRM, Financeiro)

**Stack:** Flask · Tailwind · Docker Compose · PostgreSQL (planejado, hoje SQLite) · GitHub Actions · NGINX/Gunicorn  
**Demo:** https://www.vrashows.com.br/agilizadj · Login: `admin` · Senha: `021150`

## Problema
Unificar operação de eventos (agenda), relacionamento (CRM) e financeiro em um fluxo único.

## Solução
- App SaaS multi-módulos com RBAC, dashboards e automações
- Deploy containerizado (Docker Compose) com NGINX + TLS/HTTP2
- Pipeline **CI/CD** (GitHub Actions): build, testes e deploy

## Arquitetura (alto nível)
Client (Tailwind) → Flask + RBAC → Services (Agenda, CRM, Financeiro)
                        │
                    Auth & Logs
                        │
        Docker Compose → NGINX (TLS) → Gunicorn
                        │
                 VM Cloud + Backups

## CI/CD (exemplo)
```yaml
name: deploy-agilizavra
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with: { python-version: '3.12' }
      - run: pip install -r requirements.txt
      - run: pytest -q
      - run: docker compose build --no-cache
      - name: Deploy
        run: ssh -o StrictHostKeyChecking=no $SSH_HOST 'docker compose up -d --build'


4) **Commit changes**.

### 3.2 VRASHOWS (site E2E)
1) Novo repo: `vrashows-site` → Public → Add a README → Create  
2) README:

```md
# VRASHOWS — Site Institucional (end-to-end)

**Escopo técnico:** domínio, DNS, VM Linux, **NGINX + TLS/HTTP2**, e-mail, deploy, SEO/OG, analytics, formulários e integrações.  
**Tecnologias:** Tailwind, HTML/JS, NGINX, Certbot, GitHub Actions (deploy opcional)

## Infra
- Registro de domínio e configuração de **DNS**
- Provisionamento de VM, hardening básico e firewall
- NGINX como reverse proxy, **SSL/TLS** (Let's Encrypt)
- Logs, backups e monitoramento básico

## Front-end
- Layout responsivo (A11y AA), microinterações
- Metatags Open Graph/Twitter, sitemap/robots

## Estrutura

