---
name: ad-creative
description: "Geracao de criativos para anuncios — headlines, textos, variacoes de angulo, A/B tests. Integracao com Content Studio (uma_engine). Padrao dark/green."
user-invocable: true
allowed-tools:
  - Read
  - Write
  - Edit
  - Bash
  - Grep
  - Glob
  - WebSearch
---

# Ad Creative — Skill de Geracao de Criativos para Anuncios

## Contexto

**Marca:** YOUR_COMPANY — @your-handle
**Produto principal:** Seu Produto/Desafio + Mentoria YOUR_COMPANY
**Content Studio:** `~/content-studio/`
**Engines:** `uma_engine.py`, `uma_engine_v2.py`

---

## Regras Inviolaveis

1. **SEMPRE usar acentos e cedilha** — a, e, c, o, i, u, a, e, o. Verificar CADA palavra.
2. **Formato padrao:** 1080x1920 (9:16) para Stories/Reels ads. So usar 1080x1080 se explicitamente solicitado.
3. **NUNCA recortar foto de dentro de outro criativo** — usar foto raw original ou estilo sem foto (tipografia pura).
4. **NUNCA usar a mesma imagem em multiplos criativos** — cada peca precisa de visual unico.
5. **Design campeao:** Fundo escuro (#0D0D0D ou #1A1A1A) + destaques verde (#00FF88 ou #39FF14) + texto branco.

---

## Estrutura de Copy para Anuncios

### Anatomia Completa de um Anuncio Meta

```
+-------------------------------------+
| PRIMARY TEXT (texto principal)        |
| Maximo: 125 caracteres visiveis      |
| (antes do "Ver mais")                |
| Total recomendado: 300-500 chars     |
+-------------------------------------+
| CRIATIVO (imagem ou video)           |
| 1080x1920 (9:16) ou 1080x1080 (1:1) |
+-------------------------------------+
| HEADLINE (titulo abaixo da imagem)   |
| Maximo: 40 caracteres                |
+-------------------------------------+
| DESCRIPTION (descricao)              |
| Maximo: 30 caracteres                |
+-------------------------------------+
| CTA BUTTON (botao)                   |
| "Saiba Mais" / "Inscreva-se"         |
+-------------------------------------+
```

### Framework de Copy: Hook > Problema > Solucao > Prova > CTA

| Bloco | Funcao | Exemplo |
|-------|--------|---------|
| **Hook** (1 linha) | Parar o scroll | "Eu sai de R$3K para R$30K em 90 dias usando IA." |
| **Problema** (1-2 linhas) | Gerar identificacao | "Se voce e CLT ganhando pouco e sente que tem potencial para mais..." |
| **Solucao** (2-3 linhas) | Apresentar a saida | "Existe um mercado invisivel onde profissionais comuns estao faturando com IA — sem precisar ser programador." |
| **Prova** (1-2 linhas) | Credibilizar | "Mais de 200 pessoas ja se inscreveram no desafio gratuito." |
| **CTA** (1 linha) | Acao clara | "Clique abaixo e garanta sua vaga agora. E 100% gratuito." |

---

## Framework de Variacao de Angulos

### Conceito
Mesmo produto, mesma oferta, diferentes portas de entrada. Cada angulo ataca um motivador diferente do publico.

### Angulos Validados

#### Angulo 1: Dinheiro Direto (CAMPEAO)
- **Motivador:** Ganancia / ambicao financeira
- **Hook:** "De R$3K a R$30K/mes com IA"
- **Prova:** Numeros reais, dados financeiros
- **Design:** Bold numbers em verde sobre fundo escuro
- **CPL medio:** R$2.98 - R$4.25
- **Status:** Baseline para comparacao

#### Angulo 2: Oportunidade Oculta
- **Motivador:** Curiosidade / FOMO
- **Hook:** "O mercado que 97% das pessoas nao conhecem"
- **Prova:** Dados de mercado, tamanho da oportunidade
- **Design:** Elemento de misterio, revelacao progressiva

#### Angulo 3: Medo de Ficar Para Tras
- **Motivador:** Aversao a perda
- **Hook:** "Enquanto voce pensa, outros ja estao lucrando com IA"
- **Prova:** Velocidade de mudanca, quem ja entrou
- **Design:** Contraste antes/depois, urgencia visual

#### Angulo 4: Transformacao Pessoal
- **Motivador:** Aspiracao / identidade
- **Hook:** "De empregado frustrado a especialista em IA"
- **Prova:** Jornada pessoal, depoimentos
- **Design:** Foto pessoal, storytelling visual

#### Angulo 5: Simplicidade / Sem Barreiras
- **Motivador:** Remocao de objecao
- **Hook:** "Voce nao precisa saber programar para ganhar com IA"
- **Prova:** Exemplos de pessoas comuns
- **Design:** Clean, acessivel, sem jargao

#### Angulo 6: Autoridade / Dados
- **Motivador:** Confianca / logica
- **Hook:** "Testei 47 ferramentas de IA. Essas 3 geram dinheiro real."
- **Prova:** Dados, testes, comparacoes
- **Design:** Infografico, dados visuais

---

## Geracao em Batch

### Processo para Criar Lote de Criativos

**Passo 1: Definir o lote**
```yaml
campanha: "V{N} {Tipo}"
angulo_principal: "Dinheiro Direto"
quantidade: 5 variacoes
formato: 1080x1920
destino: Landing Page do Desafio
```

**Passo 2: Gerar variacoes**
Para cada criativo, variar:
- **Hook:** 5 versoes diferentes do mesmo angulo
- **Visual:** Imagem diferente para cada um
- **CTA:** 2-3 variacoes de chamada para acao
- **Headline:** 5 opcoes curtas (max 40 chars)

**Passo 3: Nomenclatura A/B**
```
Peca {N}{Letra} — {Angulo curto}
Exemplo:
- Peca 5A — Mesa de Dinheiro (imagem de notas + IA)
- Peca 5B — Bold Numbers (tipografia grande R$30K)
- Peca 5C — Laptop Glow (tela com dashboard)
- Peca 5D — Antes Depois (split visual)
- Peca 5E — Data Chart (grafico crescente)
```

**Passo 4: Documentar**
Cada criativo deve ter registro:
```yaml
peca: "5A"
nome: "Mesa de Dinheiro"
angulo: "Dinheiro Direto"
hook: "Eu sai de R$3K para R$30K em 90 dias usando IA"
headline: "Descubra o Mercado Invisivel"
description: "Desafio gratuito de 5 dias"
cta_button: "Saiba Mais"
imagem: "descricao visual do criativo"
formato: "1080x1920"
```

---

## Templates de Copy por Angulo

### Template: Dinheiro Direto
```
PRIMARY TEXT:
{Valor baixo} → {Valor alto} em {periodo} usando IA.

Parece mentira? Eu tambem achava.

Mas existe um mercado invisivel onde profissionais comuns estao {resultado} usando ferramentas de inteligencia artificial — sem precisar ser programador, sem investir fortunas.

{Prova social: X pessoas ja se inscreveram}

Eu criei um desafio GRATUITO de 5 dias para te mostrar exatamente como funciona.

{CTA: Clique e garanta sua vaga}

HEADLINE: {Frase curta com valor} (max 40 chars)
DESCRIPTION: Desafio gratuito de 5 dias
CTA: Saiba Mais
```

### Template: Oportunidade Oculta
```
PRIMARY TEXT:
97% dos empreendedores nao sabem que esse mercado existe.

{Dado surpreendente sobre o mercado de IA}

Enquanto a maioria esta brigando por migalhas nos mesmos nichos saturados, um grupo pequeno esta {resultado} em um mercado que ninguem olha.

Eu vou te mostrar exatamente qual e esse mercado em um desafio GRATUITO de 5 dias.

{Prova social}

{CTA}

HEADLINE: O Mercado Invisivel da IA
DESCRIPTION: Vagas limitadas
CTA: Saiba Mais
```

### Template: Medo / Urgencia
```
PRIMARY TEXT:
Cada dia que passa, mais pessoas estao descobrindo como ganhar dinheiro com IA.

E cada dia que voce espera, mais dificil fica entrar.

{Dado de velocidade de crescimento}

Nao estou dizendo isso para te assustar. Estou dizendo porque eu ja vi esse filme antes — {referencia a outra onda tecnologica}.

Quem entrou primeiro, lucrou mais.

{CTA para desafio gratuito}

HEADLINE: Nao fique para tras
DESCRIPTION: Comeca em {data}
CTA: Inscreva-se
```

---

## Integracao com Content Studio

### Geracao Programatica
```bash
# Usando uma_engine_v2.py para gerar criativos
cd ~/content-studio
python uma_engine_v2.py --template ad_creative \
  --angle "dinheiro_direto" \
  --format "1080x1920" \
  --variations 5 \
  --output ./output/ads/
```

### Parametros do Engine
| Parametro | Valores |
|-----------|---------|
| `--template` | `ad_creative`, `carousel`, `story`, `reel_cover` |
| `--angle` | `dinheiro_direto`, `oportunidade`, `medo`, `transformacao`, `simplicidade`, `autoridade` |
| `--format` | `1080x1920`, `1080x1080` |
| `--variations` | 1-10 |
| `--style` | `dark_green` (padrao), `clean_white`, `gradient` |

---

## Checklist de Qualidade — Criativo

Antes de publicar qualquer criativo:

- [ ] Acentuacao correta em TODAS as palavras
- [ ] Formato correto (1080x1920 ou conforme solicitado)
- [ ] Texto ocupa menos de 20% da imagem
- [ ] Foto original (nao recortada de outro criativo)
- [ ] Visual diferente de outros criativos ativos
- [ ] Hook legivel nos primeiros 3 segundos
- [ ] CTA claro e visivel
- [ ] Cores da marca (dark + green)
- [ ] Sem erros gramaticais
- [ ] Headline dentro do limite (40 chars)
- [ ] Description dentro do limite (30 chars)
- [ ] Nomenclatura correta (Peca XY — Nome)
