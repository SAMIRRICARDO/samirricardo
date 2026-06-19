<div align="center">

# Samir Ricardo

**AI Systems Architect · Fundador VRASHOWS · Criador do Human RAG**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-samir--ricardo-0A66C2?logo=linkedin&logoColor=white&style=flat-square)](https://linkedin.com/in/samir-ricardo-almeida-b23b3825b)
[![Email](https://img.shields.io/badge/Email-contato@vrashows.com.br-EA4335?logo=gmail&logoColor=white&style=flat-square)](mailto:contato@vrashows.com.br)
[![Livro](https://img.shields.io/badge/Amazon-O%20Maior%20Ativo-FF9900?logo=amazon&logoColor=white&style=flat-square)](https://a.co/d/0dTw8I9Y)

</div>

---

## VRAXIA Sense — IA Perceptiva

> *"IA tradicional responde quando você pergunta. VRAXIA Sense percebe antes de você notar."*

```
IA tradicional:   você pergunta  →  ela responde
VRAXIA Sense:     evento acontece  →  ela percebe  →  ela age
```

**VRAXIA Sense** é uma camada de percepção proativa — middleware de inteligência que monitora sinais do mundo externo (eventos, mensagens, métricas, prazos) e age de forma autônoma, **antes que um humano precise notar**.

### O Pipeline de 3 Níveis

```
 EVENTO  →  NÍVEL 0  →  NÍVEL 1  →  NÍVEL 2  →  NOTIFICAÇÃO
           Filtro        Triagem    Classificação   Telegram
           $0,0000       ~$0,0001    ~$0,0003       (handoff)
           CPU puro      Haiku       Haiku
           70-80%        filtra      filtra
           eliminados    ~60%        ~80%
```

| Métrica | Meta | Produção |
|---|---|---|
| Eventos eliminados no Nível 0 | >70% | **76%** |
| Custo médio por evento bruto | <$0,001 | **$0,000034** |
| Latência evento → notificação | <2 min | **~8 segundos** |
| Taxa de falsos positivos | <10% | **~6%** |
| Custo a 1.000 eventos/dia | — | **~$1,02/mês** |

**Piloto comercial em produção:** Monitora replies de LinkedIn (Waalaxy) e classifica leads B2B automaticamente antes de qualquer humano abrir a caixa de entrada.

**→ [github.com/SAMIRRICARDO/vraxia-sense](https://github.com/SAMIRRICARDO/vraxia-sense)**

---

## Human RAG

```
RAG tradicional  →  indexa documentos  →  recupera texto
Human RAG        →  indexa raciocínio  →  reconstrói decisões
```

**75% das empresas familiares brasileiras fecham após a saída do fundador** — não por falta de capital, mas por perda de conhecimento estratégico (PwC).

RAG tradicional indexa **o que foi escrito**.  
Human RAG indexa **como a pessoa pensa e decide**.

Implementado no **VRAXIA OS** — plataforma enterprise com 8 agentes departamentais em produção.

| Métrica | Resultado |
|---|---|
| ↓ Custo de inferência | **80%** |
| ↑ Eficiência operacional | **40%** |
| ↓ Falhas por contexto perdido | **30%** |

---

## VRAXIA OS — Enterprise AI Platform

```
VRAXIA OS
├── Module Agents       — 8 agentes departamentais (Comercial, Financeiro, Jurídico...)
├── Skill Registry      — 1.161+ skills indexadas
├── Codex Lead Engine   — find_new_leads · enrich_company · validate_leads
├── VRAXIA Sense    ←   — camada de percepção proativa
└── Multi-Tenant BYOK   — cada cliente usa suas próprias API keys
```

**→ [github.com/SAMIRRICARDO/ai-cognitive-runtime](https://github.com/SAMIRRICARDO/ai-cognitive-runtime)**

### Agentes em Produção

| Camada | Agente | Função |
|---|---|---|
| **Percepção** | `sense` | Monitora eventos, filtra ruído, notifica handoffs |
| **Comercial** | `lead-enrichment` | Enriquece leads com decisores e contatos |
| **Comercial** | `outreach` | Gera outreach personalizado por perfil |
| **Comercial** | `lead-classifier` | Qualifica respostas (variantes A–E, intent, score) |
| **Comercial** | `codex` | Busca, enriquece e valida leads via Tavily + LLM |
| **Orquestração** | `coordinator` | Decompõe tarefas em DAGs, gerencia execução |
| **Pesquisa** | `researcher` | Web intelligence, fact-finding, mercado |
| **Memória** | `vault` | Busca semântica no Human RAG (Obsidian) |

### Pipeline Outbound

```
Pesquisa (Tavily)  →  Enriquecimento (decisores/emails)  →  Validação (40+ empresas)
       ↓
Outreach (template por perfil)  →  Disparo (Resend)  →  Classificação (reply → CRM)
```

---

## Memória Multi-Camada

```
Redis          →  cache curto prazo, dedup, custo acumulado
PostgreSQL     →  memória semântica longo prazo (pgvector)
SQLite         →  cache local offline
Obsidian Vault →  Human RAG — memória arquitetural e decisional
```

---

## Stack

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white&style=flat-square)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white&style=flat-square)
![Claude](https://img.shields.io/badge/Claude%20Haiku%2FSonnet-D4A017?logo=anthropic&logoColor=white&style=flat-square)
![PostgreSQL](https://img.shields.io/badge/pgvector-4169E1?logo=postgresql&logoColor=white&style=flat-square)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white&style=flat-square)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white&style=flat-square)
![Resend](https://img.shields.io/badge/Resend-000000?style=flat-square)
![Telegram](https://img.shields.io/badge/Telegram-26A5E4?logo=telegram&logoColor=white&style=flat-square)

**Arquitetura:** ESM · Express + SSE · RAG local (JSONL) · BYOK multi-tenant  
**Observabilidade:** token usage · latência · custo por agente · workflow tracing  
**Governança:** cheap mode · seleção dinâmica de modelo · caps de batch por domínio

---

## Publicação

**[O Maior Ativo da Sua Empresa — E por que ele está indo embora?](https://a.co/d/0dTw8I9Y)**  
Amazon KDP · Junho 2026 · O primeiro livro brasileiro sobre Human RAG aplicado à preservação de conhecimento organizacional.

---

<div align="center">
<sub>VRASHOWS · contato@vrashows.com.br · (11) 95357-7804</sub>
</div>
