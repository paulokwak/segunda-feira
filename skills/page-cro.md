---
name: page-cro
description: "Otimizacao de landing pages (CRO) — framework 7 pontos, mobile-first, above-the-fold, velocidade, A/B testing, hierarquia visual, tratamento de objecoes."
user-invocable: true
allowed-tools:
  - Read
  - Write
  - Edit
  - Bash
  - Grep
  - Glob
  - WebSearch
  - WebFetch
  - mcp__playwright__browser_navigate
  - mcp__playwright__browser_snapshot
  - mcp__playwright__browser_take_screenshot
  - mcp__playwright__browser_evaluate
---

# Page CRO — Skill de Otimizacao de Landing Pages

## Contexto

**Padrao visual:** Dark (#0D0D0D) + Green (#00FF88) + White text
**Trafego:** 70%+ mobile (Meta Ads → Instagram/Facebook)

---

## Framework CRO — 7 Pontos

### Ponto 1: Proposta de Valor (Value Proposition)

**Checklist:**
- [ ] O beneficio principal e claro em 1 frase
- [ ] O "para quem" esta explicito
- [ ] O "como funciona" e intuitivo
- [ ] Diferencial esta evidente

**Formula:**
```
[Resultado desejado] + [Para quem] + [Sem a maior objecao]
Exemplo: "Fature com IA em 5 dias — sem saber programar"
```

**Teste:** Mostre a headline para alguem por 5 segundos. Se nao entender o que e e para quem, reescrever.

### Ponto 2: Headline e Sub-headline

**Headline:** Promessa principal — maximo 10 palavras

| Tipo | Exemplo | Quando Usar |
|------|---------|-------------|
| Beneficio direto | "Fature R$10K/mes com Inteligencia Artificial" | Publico quente |
| Curiosidade | "O Mercado Invisivel que Gera R$30K/mes" | Publico frio |
| Prova social | "600+ Pessoas Ja Descobriram Como Lucrar com IA" | Retargeting |
| Pergunta | "E Se Voce Pudesse Ganhar Dinheiro com IA?" | Topo de funil |

**Regras:**
- Headline e sub-headline devem funcionar sozinhas
- Fonte grande e bold para headline (minimo 28px mobile)
- Contraste alto (branco sobre escuro ou verde sobre escuro)
- SEMPRE com acentos corretos

### Ponto 3: CTA (Call to Action)

**Checklist do CTA perfeito:**
- [ ] Texto de acao (verbo): "Quero Participar Gratuitamente"
- [ ] Cor contrastante (verde #00FF88 sobre fundo escuro)
- [ ] Tamanho grande (minimo 48px altura no mobile)
- [ ] Espaco em volta (padding generoso)
- [ ] Micro-copy abaixo: "100% gratuito. Sem cartao de credito."
- [ ] Presente acima da dobra E repetido a cada 2-3 secoes
- [ ] Apenas UM tipo de CTA na pagina

### Ponto 4: Hierarquia Visual

**Layout Mobile-First:**
```
┌──────────────────────────┐
│       [Logo pequeno]      │
│                           │
│    HEADLINE GRANDE        │
│    Sub-headline menor     │
│                           │
│  ┌──────────────────────┐ │
│  │  [BOTAO CTA VERDE]   │ │
│  └──────────────────────┘ │
│  "100% gratuito"          │
│                           │
│  ✓ Beneficio 1            │
│  ✓ Beneficio 2            │
│  ✓ Beneficio 3            │
│                           │
│  "600+ ja se inscreveram" │
│  [Depoimento 1]           │
│                           │
│  ┌──────────────────────┐ │
│  │  [BOTAO CTA VERDE]   │ │
│  └──────────────────────┘ │
│                           │
│  FAQ / Objecoes           │
│                           │
│  ┌──────────────────────┐ │
│  │  [BOTAO CTA VERDE]   │ │
│  └──────────────────────┘ │
│  [Footer minimo]          │
└──────────────────────────┘
```

**Regras de design:**
- Fundo escuro (#0D0D0D ou #1A1A1A)
- Texto branco (#FFFFFF) para corpo
- Verde (#00FF88 ou #39FF14) para destaques e botoes
- Uma coluna no mobile (NUNCA grids complexos)
- Espacamento generoso (minimo 40px entre secoes)
- Sem menu de navegacao
- Sem pop-ups intrusivos

### Ponto 5: Prova Social

| Elemento | Impacto | Implementacao |
|----------|---------|---------------|
| Contador de inscritos | Alto | Numero atualizado |
| Depoimentos com foto | Muito alto | 2-3 curtos, com nome e resultado |
| Depoimentos em video | Maximo | Embed de video curto (30-60s) |
| Screenshots de resultado | Alto | Print de dashboard, pagamento |

**Regras:**
- Depoimentos REAIS apenas
- Incluir resultado especifico
- Foto real da pessoa
- Atualizar numeros conforme crescem

### Ponto 6: Tratamento de Objecoes

**As 7 objecoes mais comuns (mercado BR de infoprodutos):**

| # | Objecao | Resposta |
|---|---------|----------|
| 1 | "E gratuito mesmo?" | "Sim. 100% gratuito. Sem cartao de credito." |
| 2 | "Preciso saber programar?" | "Nao. As ferramentas sao visuais e intuitivas." |
| 3 | "Nao tenho tempo" | "Sao apenas 50 minutos por dia durante 5 dias." |
| 4 | "Funciona para meu nicho?" | "IA se aplica a qualquer area de negocio." |
| 5 | "Ja tentei e nao deu certo" | "Esse metodo e diferente. Foco em resultados praticos." |
| 6 | "E confiavel?" | "X pessoas ja participaram. Veja os depoimentos." |
| 7 | "Vou receber gravacao?" | "Replay disponivel por 24h apos cada aula." |

### Ponto 7: Reducao de Atrito (Friction)

- [ ] Formulario com maximo 2 campos (Nome + WhatsApp)
- [ ] Sem captcha visivel (usar reCAPTCHA v3 invisivel)
- [ ] Sem redirecionamentos desnecessarios
- [ ] SSL ativo (https://)
- [ ] Sem erros de console
- [ ] Sinal de seguranca: "Seus dados estao protegidos"

---

## Mobile-First Checklist

- [ ] **Tap targets:** Botoes com minimo 48x48px
- [ ] **Font size:** Minimo 16px para corpo
- [ ] **Espacamento:** Minimo 8px entre elementos clicaveis
- [ ] **Imagens:** Responsivas (max-width: 100%)
- [ ] **Scroll:** Vertical apenas
- [ ] **Gestos:** Nao depende de hover

---

## Velocidade de Carregamento

### Metas
| Metrica | Meta | Ferramenta |
|---------|------|------------|
| LCP | < 2.5s | PageSpeed Insights |
| FID | < 100ms | PageSpeed Insights |
| CLS | < 0.1 | PageSpeed Insights |
| Tempo total | < 3s | GTmetrix |
| Tamanho da pagina | < 1MB | DevTools |

### Otimizacoes Prioritarias

| Acao | Impacto | Esforco |
|------|---------|---------|
| Converter imagens para WebP | Alto | Baixo |
| Lazy loading abaixo da dobra | Alto | Baixo |
| Minificar CSS/JS | Medio | Baixo |
| Comprimir com Gzip/Brotli | Alto | Medio |
| Eliminar JS nao utilizado | Alto | Medio |
| CDN para assets estaticos | Alto | Medio |

---

## Metodologia de A/B Testing

### O que Testar (em ordem de impacto)

| Prioridade | Elemento | Variacao Tipica |
|-----------|----------|-----------------|
| 1 (maior) | Headline | Beneficio vs Curiosidade vs Prova Social |
| 2 | CTA (texto) | "Participar Gratuitamente" vs "Garantir Minha Vaga" |
| 3 | CTA (cor) | Verde vs Laranja vs Branco |
| 4 | Layout acima da dobra | Com imagem vs Sem imagem |
| 5 | Prova social | Numero vs Depoimento vs Ambos |

### Regras de A/B Test

1. **Testar UMA variavel por vez**
2. **Volume minimo:** 100 conversoes por variacao
3. **Duracao minima:** 7 dias
4. **Significancia estatistica:** 95% de confianca
5. **Nao espiar resultados** antes do volume minimo
6. **Documentar TUDO:** hipotese, variacoes, resultados, aprendizado
