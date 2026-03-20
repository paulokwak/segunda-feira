# Segunda-feira

**47 agentes de IA. 20 skills. 7 rules. O terror do CLT.**

---

## O que é

Segunda-feira é um framework de orquestração de agentes de IA para desenvolvimento full-stack e operações de negócio. Ele define **47 agentes especializados** organizados em **8 departamentos**, cada um com:

- **Job Description** completo (cargo, missão, KPIs, autoridade, restrições)
- **POP (Procedimento Operacional Padrão)** — passo a passo de como o agente executa seu trabalho
- **SIPOC** (Supplier-Input-Process-Output-Customer) — mapa de interações

Projetado para rodar com [Claude Code](https://docs.anthropic.com/en/docs/claude-code) da Anthropic, transformando um único terminal em uma empresa inteira de agentes de IA.

## Por que o nome

Porque segunda-feira é o dia que todo mundo odeia — mas os agentes amam. Enquanto você toma café, 47 agentes já estão trabalhando.

---

## O que está incluído

### Agentes Core (`commands/`)
38 agentes com personas, comandos e workflows definidos:

| Agente | Role | Modelo |
|--------|------|--------|
| Nexo | Chief of Staff | opus |
| Orion | Master Orchestrator | opus |
| Advisory Board | Conselho Consultivo (11 conselheiros) | opus |
| Morgan | Product Manager | opus |
| Dex | Senior Engineer | sonnet |
| Quinn | Test Architect (QA) | opus |
| Aria | System Architect | opus |
| Gage | DevOps Engineer | sonnet |
| Dara | Data Engineer | sonnet |
| Pax | Product Owner | opus |
| River | Scrum Master | haiku |
| Craft | Squad Creator | sonnet |
| Uma | UX Design Expert | sonnet |
| Trig | Gestor de Tráfego Pago | sonnet |
| Luna | Estrategista de Conteúdo | sonnet |
| Dash | Produtor de Vídeo com IA | sonnet |
| Copywriter | Copy Persuasivo Multi-Canal | sonnet |
| Creative Director | Direção Criativa | sonnet |
| CRO Specialist | Otimização de Conversão | sonnet |
| Max | Gestor Comercial Estratégico | opus |
| Nico | Head de Vendas | sonnet |
| Primo | SDR | haiku |
| Apex | Closer High-Ticket | sonnet |
| Zap | WhatsApp Marketing Specialist | sonnet |
| Nova | CFO | opus |
| Flex | Assistente Financeiro | haiku |
| Finn | Monitor de Plataformas Financeiras | haiku |
| Care | Customer Success | haiku |
| Pulse | CS Retention Specialist | sonnet |
| Ori | Operations Manager | sonnet |
| Sentinel | Operations Monitor | haiku |
| Workflow Orchestrator | Orquestrador Multi-Step | opus |
| Kai | Product Manager (Produtos Digitais) | opus |
| Sage | Mentor Educacional | haiku |
| Eve | Events Manager | haiku |
| Atlas | Business Analyst | sonnet |
| Market Intel | Inteligência Competitiva | opus |
| Launch Strategist | Estrategista de Lançamentos | opus |

### Agentes Especialistas (`agents/`)
16 agentes com subagent definitions para domínios específicos:

| Agente | Persona | Domínio |
|--------|---------|---------|
| Automation Architect | Wire | n8n, Make, webhooks, pipelines |
| Cold Outreach | Hunter | Prospecção B2B, cold email |
| Copywriter | — | Copy persuasivo, ads, LPs |
| Creative Director | — | Direção criativa, criativos ads |
| CRO Specialist | — | Otimização de conversão |
| Growth Hacker | Surge | Algoritmos sociais, crescimento |
| Launch Strategist | — | Estratégia de lançamento |
| Market Intel | — | Inteligência de mercado |
| Offer Engineer | Forge | Ofertas irrecusáveis, stack de valor |
| Prompt Engineer | Prism | Prompts avançados, safety |
| RAG Architect | Sage | RAG, vector stores, memória dual |
| Swarm Simulator | Swarm | MiroFish, simulação multi-agente |
| Vibe Coder | Blast | B.L.A.S.T., context engineering |
| Voice AI Specialist | Vox | Voice AI, dublagem, TTS, ASR |
| WhatsApp Specialist | Zap | WhatsApp Bot, automações |
| Workflow Orchestrator | — | Workflows multi-step |

### Skills (`skills/`)
20 skills especializadas que os agentes podem invocar:

| Skill | Descrição |
|-------|-----------|
| `ad-creative` | Geração de criativos para anúncios Meta Ads |
| `agent-council` | Conselho deliberativo multi-perspectiva |
| `agent-engineer` | Projeta agentes e squads |
| `algorithm-hack` | Engenharia reversa de algoritmos sociais |
| `cold-outreach-campaign` | Campanhas cold email B2B |
| `copywriting` | Copy persuasivo — AIDA, PAS, BAB, hooks, CTAs |
| `launch-strategy` | Estratégia de lançamento digital em 5 fases |
| `lead-magnets` | Criação de iscas digitais e LPs de captação |
| `marketing-psychology` | 18 gatilhos mentais e persuasão ética |
| `n8n-workflows` | Biblioteca de workflows n8n prontos |
| `offer-optimizer` | Framework 4-critérios + stack Hormozi |
| `ops-catalog` | Catálogo operacional de ferramentas e scripts |
| `page-cro` | Otimização de landing pages (CRO) — 7 pilares |
| `paid-ads` | Gestão de tráfego pago Meta Ads (metodologia Sobral) |
| `rag-builder` | Pipelines RAG de produção |
| `skill-creator` | Cria skills modulares padrão |
| `social-content` | Conteúdo para Instagram — posts, reels, carrosséis |
| `swarm-simulation` | Simulação MiroFish multi-agente |
| `voice-dubbing` | Pipeline de dublagem 10 etapas |
| `vps-setup` | Setup VPS Docker completo |

### Comandos Operacionais (`commands/`)
7 comandos standalone para operações do dia a dia:

| Comando | Descrição |
|---------|-----------|
| `/analyze-competitors` | Análise competitiva completa de concorrentes |
| `/campaign-report` | Relatório de campanha Meta Ads com análise Sobral/Hormozi |
| `/conteudo-semanal` | Pesquisa + estratégia + criativos + upload Instagram |
| `/fix-instagram` | Diagnostica e corrige posts Instagram falhos |
| `/plan-launch` | Planeja lançamento digital completo |
| `/research` | Pesquisa profunda multi-fonte |
| `/whatsapp-bot` | Gerencia WhatsApp Bot com Claude AI |

### Estrutura Organizacional (`organization/`)
8 departamentos com POPs e SIPOCs completos:

| Departamento | Agentes | Foco |
|-------------|---------|------|
| Diretoria | Nexo, Orion, Advisory Board | Estratégia, governança, orquestração |
| Engenharia | Morgan, Dex, Quinn, Aria, Gage, Dara, Pax, River, Craft, Uma | Desenvolvimento full-stack |
| Marketing & Conteúdo | Trig, Luna, Dash, Copywriter, Creative Director, CRO Specialist | Demanda e autoridade de marca |
| Comercial & Vendas | Max, Nico, Primo, Apex, Zap | Pipeline de vendas |
| Financeiro | Nova, Flex, Finn | Saúde financeira |
| CS & Retenção | Care, Pulse | Satisfação e retenção |
| Operações | Ori, Sentinel, Workflow Orchestrator | Processos e infraestrutura |
| Produto & Educação | Kai, Sage, Eve, Atlas, Market Intel, Launch Strategist | Produtos digitais e eventos |

### Rules (`rules/`)
7 regras que governam o framework:

| Rule | Governa |
|------|---------|
| `workflow-execution.md` | SDC phases, QA Loop, Spec Pipeline, Brownfield Discovery |
| `story-lifecycle.md` | Status progression, validation checklist, QA gate decisions |
| `agent-authority.md` | Delegation matrix — quem pode fazer o quê |
| `ids-principles.md` | REUSE > ADAPT > CREATE hierarchy |
| `coderabbit-integration.md` | Self-healing config, severity handling |
| `external-api-patterns.md` | SYNC > CACHE > REAL-TIME for API integrations |
| `mcp-usage.md` | MCP server governance and tool selection |

---

## Como usar

### Pré-requisitos

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) instalado
- Node.js 18+
- Git

### Instalação

```bash
# Clone o repositório
git clone https://github.com/YOUR_USERNAME/segunda-feira.git

# Copie os arquivos para sua configuração Claude Code
cp -r segunda-feira/commands/ ~/.claude/commands/
cp -r segunda-feira/agents/ ~/.claude/agents/
cp -r segunda-feira/skills/ ~/.claude/skills/
cp -r segunda-feira/rules/ ~/.claude/rules/
cp -r segunda-feira/organization/ ~/.claude/organization/
cp segunda-feira/CLAUDE.md ~/.claude/CLAUDE.md
```

### Uso básico

```bash
# No Claude Code, ative um agente
@dev           # Ativa o engenheiro sênior
@content       # Ativa a estrategista de conteúdo
@aios-master   # Ativa o master orchestrator

# Use comandos de agente
*help          # Mostra comandos disponíveis
*create-story  # Cria nova story
*task dev-develop-story  # Executa task de desenvolvimento

# Use skills
/paid-ads      # Gestão de tráfego pago
/copywriting   # Copy persuasivo
/launch-strategy  # Estratégia de lançamento
```

### Personalização

Os agentes usam placeholders que você deve substituir:

| Placeholder | Substitua por |
|------------|--------------|
| `@your-handle` | Seu @ do Instagram |
| `your-domain.com` | Seu domínio |
| `YOUR_COMPANY` | Nome da sua empresa |
| `YOUR_NAME` | Seu nome |
| `YOUR_PIXEL_ID` | Seu Pixel Meta |
| `YOUR_PAGE_ID` | Seu Page ID Meta |
| `YOUR_APP_PATH` | Path da sua aplicação |
| `YOUR_VPS_IP` | IP do seu servidor |
| `YOUR_VPS_PASSWORD` | Senha do seu servidor |
| `YOUR_BOT_PORT` | Porta do seu bot |

---

## Estrutura do repositório

```
segunda-feira/
├── README.md
├── CLAUDE.md
├── agents/                            # 16 agentes especialistas
├── commands/                          # 38 agentes core + 7 operacionais
├── skills/                            # 20 skills invocáveis
├── organization/                      # 8 departamentos
└── rules/                             # 7 regras do framework
```

---

## Metodologias integradas

- **Pedro Sobral** — Escala e pausa de campanhas Meta Ads
- **Alex Hormozi** — Ofertas irrecusáveis e escala
- **Brian Manon** — Criativos de alta performance
- **Motion** — Analytics de criativos
- **SPIN Selling** — Discovery e fechamento high-ticket
- **CodeRabbit** — Self-healing de código com análise estática
- **IDS (Incremental Development System)** — REUSE > ADAPT > CREATE
- **MiroFish** — Simulação multi-agente e inteligência coletiva
- **B.L.A.S.T.** — Context engineering para desenvolvimento AI-first

---

## Licença

MIT License — use, modifique e distribua livremente.

---

*Segunda-feira v5.0 — 47 agentes de IA. 20 skills. O terror do CLT.*
