# Sena Comercial — Design System

> **"Brigar por cada milésimo de segundo que coloca seu negócio no topo do pódio."**
> — Brandbook Sena, Fase 2

A Sena Comercial é uma agência de **estruturação comercial e marketing** para PMEs — com foco em **imobiliárias, construtoras e incorporadoras**. A marca se posiciona como uma "escuderia de elite" para empresários: precisão matemática, transparência brutal, zero enrolação.

Este design system traduz esse DNA em tokens, componentes e templates de UI prontos para usar em landing pages, decks de oferta, dashboards, anúncios e materiais internos.

---

## Contexto da marca

- **Nome:** Sena Comercial (wordmark: **SENA — EXPANSÃO COMERCIAL**)
- **Fundador:** Airton Carneiro (referência simbólica ao Ayrton Senna — instinto de campeão, alta performance)
- **Produto estrela:** **MaVIS** — Máquina de Vendas Imobiliárias da Sena
- **Arquétipo:** O Herói (primário) + O Governante com traços de Rebelde (secundário)
- **Palavra que queremos possuir:** "ESTRUTURAÇÃO" / "RESULTADO‑CRU"
- **Metáfora central:** Escuderia de Fórmula 1 — telemetria, box, pódio, milésimo de segundo, pista

### O inimigo que combatemos
Amadorismo comercial, "falsa consultoria", agências que vendem métricas de vaidade em vez de vendas reais, "enrolação".

---

## Fontes utilizadas (consumidas deste repo)

Todos os arquivos originais estão espelhados em `source_docs/`:

| Origem | Papel |
|---|---|
| `Brandbook Sena.pdf` | **Fonte canônica** da identidade: paleta, tipografia, tom de voz, posicionamento |
| `MVM - TEMPLATE DE OFERTA.pdf` | Template de oferta comercial (MaVIS) — estrutura de deck de venda |
| `MVM - Mecanismo Unico Sena.pdf` | Mecanismo único do produto |
| `MVM - Tese de Mercado Sena.pdf` | Tese de mercado |
| `MVM - Estrategia de Marketing Imobiliario Assertivo Sena.pdf` | Estratégia de marketing |
| `MVM - Copy & Storytelling Master Document` (não copiado — ver caveat) | Copy master |
| `mavis-lp.html` | LP de exemplo da Masterclass MaVIS — **única implementação visual existente** e principal referência de componentes |
| `uploads/rendernet_*.png`, `uploads/Versão Final *.png` | Imagens de marca (Airton em F1, executivo, estratégia, logo) |

---

## Índice de arquivos

```
/
├── README.md                       ← você está aqui
├── SKILL.md                        ← skill file (Claude Code compatível)
├── colors_and_type.css             ← tokens CSS: cores, tipografia, espaçamento, sombras
├── assets/                         ← logos, fotos de marca, imagens
├── source_docs/                    ← PDFs originais + LP de referência (read-only)
├── preview/                        ← cards do Design System tab
│   ├── logos.html, colors-*.html, type-*.html, spacing.html,
│   ├── components-*.html, iconography.html, photography.html, ...
├── ui_kits/
│   └── mavis-landing/              ← recreation da MaVIS LP + componentes
│       ├── index.html, *.jsx, README.md
└── slides/
    └── index.html (+ slide HTMLs)  ← template de oferta MaVIS em formato deck
```

---

## Content Fundamentals

**Tom de voz: Jovial, confiante, ousado. Transparência brutal. Zero enrolação.**
(Fonte: Brandbook Fase 1.2)

- **Idioma:** Português brasileiro. Nunca traduzir termos consagrados do contexto — "lead", "CPL", "CRM", "pipeline", "closer", "ticket" permanecem em inglês. Termos proprietários vão em **itálico serifado**: *Filtro de Intencionalidade Pós-Clique*, *Lead Inerte*, *Sequestro de Atenção*, *Montanha-Russa Financeira*.
- **Pessoa:** Fala-se com o leitor na **segunda pessoa (você)**. Nunca "nós" vago. O cliente é o herói; a Sena é o guia.
- **Casing:** Sentence case em corpo. **UPPERCASE** reservado para CTAs, overlines de telemetria, gritos de impacto ("NA PRÓXIMA TERÇA — 12H"). Títulos usam Title Case em serifa display.
- **Emoji:** **Uso cirúrgico e funcional, não decorativo.** Apenas 📲 em CTAs de WhatsApp/Meet, ✅ em bullet lists de benefício, 📌 em casos/provas, 👇 como dica de fluxo. Nunca 🎉✨🚀💎🔥 etc.
- **Ponto de vista:** "A Sena é a ÚNICA que…". Posicionamento absoluto, não relativo.
- **Evitar:** promessas vagas ("potencializar", "alavancar"), superlativos sem prova ("o melhor"), jargão de consultoria ("sinergia", "holístico").
- **Favorecer:** verbos de ação ("instalar", "estruturar", "cortar"), números cravados (R$ 300 → R$ 1.000.000), metáforas de pista (telemetria, box, pódio, pole-position, milésimo).

### Exemplos canônicos do repo

> **Headline:** "Como Lotar Sua Agenda Só com *Compradores Reais — Sem Pagar Agência e Sem Atender Curioso no WhatsApp*"
>
> **Elevator pitch:** "Muitas empresas dizem estar em alta performance, mas a verdade é que as PMEs estão perdendo vendas por amadorismo operacional. Nós somos a Sena Comercial: estruturamos a sua máquina de marketing e vendas com o rigor, a verdade bruta e a precisão de uma escuderia de Elite."
>
> **Prova:** "📌 **Caso Anderson Gusmão:** R$ 300 investidos → 11 visitas hiperqualificadas em 1 semana → R$ 1.000.000 em vendas fechadas."
>
> **CTA:** "📲 Entrar no Grupo VIP" / "Agende uma Análise da sua Operação Comercial"

### Padrão de highlight
Dentro de uma headline sans-serif black, a **frase de virada** vai em `font-family: Playfair Display; font-style: italic; color: var(--sena-orange);`. Isso é a assinatura visual da marca — serifa italic laranja = "faísca".

---

## Visual Foundations

### Paleta (canonical, do Brandbook)
| Token | Hex | Papel |
|---|---|---|
| `--sena-black` | `#000000` | Fundo padrão. Toda superfície começa aqui. |
| `--sena-asphalt` | `#2C2C2C` | Cinza chumbo — cards, divisores fortes |
| `--sena-gold` | `#C5A059` | **Dourado Campeão** — CTA primário, pódio, sucesso |
| `--sena-orange` | `#E85D04` | **Alaranjado Pulsante** — ignição, números críticos, highlight italic |
| `--sena-red` | `#CC0000` | Urgência legítima ("Limite de 100 pessoas") |

**Regra de uso:** 80% preto/carbono, 15% tons de branco/creme, 5% ouro **ou** laranja (nunca os dois gritando na mesma vista). Ouro = prestígio parado. Laranja = ação / alerta / ignição.

### Tipografia
- **Display / headlines institucionais:** Playfair Display (substituindo Baskerville citado no brandbook — mesma família serifa old-style de alto contraste, disponível no Google Fonts). Pesos 700/800/900.
- **Corpo, UI, dashboards:** Montserrat (citada literalmente no brandbook).
- **Código / métricas / telemetria:** JetBrains Mono.
- **Itálico serifado** é reservado para **destaques** (nunca blocos inteiros) — confere "velocidade e grife".

### Backgrounds
- **Padrão:** preto absoluto `#000`. Dashboards em fundo escuro, métricas "acesas" em dourado/laranja (brandbook 4.4).
- **Variação 1:** grão sutil sobre preto (noise texture ~3% alpha) — evoca paddock noturno.
- **Variação 2:** foto de ambiente (Airton, box de F1) com overlay preto 70-85% e viés em B&W + um acento dourado/laranja (ver `assets/brand-racing-white-yellow.png` — monocromático com um ponto de cor).
- **Evitar:** gradientes bluish-purple, gradientes de arco-íris, fundos claros como padrão, patterns decorativos.

### Gradientes permitidos
- `linear-gradient(180deg, #000 0%, #0A0A0A 100%)` — desaturador de bordas
- `radial-gradient(circle at top, rgba(232,93,4,0.12), transparent 60%)` — "faísca" sutil atrás de CTAs
- `linear-gradient(90deg, transparent, rgba(197,160,89,0.4), transparent)` — divisores douradas

### Cards & superfícies
- Fundo: `--bg-carbon` (#0A0A0A) ou `--bg-surface` (#1A1A1A)
- Border: 1px `rgba(255,255,255,0.10)`. Hover → `rgba(197,160,89,0.35)`.
- Radius: **3–8px** no máximo. Cantos afiados = precisão. Nunca `border-radius: 24px+`.
- Shadow: discretas — `0 8px 24px rgba(0,0,0,0.45)`. Glow dourado/laranja apenas em CTA hero.

### Borders
- 1px sempre. 2–3px apenas em `border-left` de **filter-block** (padrão canônico do repo — barra lateral laranja 3px com fundo `rgba(232,93,4,0.06)`).
- Underlines e dividers preferem linha dourada translúcida a linha branca sólida.

### Layout
- Full-bleed quando a foto é protagonista (Airton, F1). Com container `max-width: 1200px` na maioria dos casos; `max-width: 520-720px` em LP de conversão (ver `mavis-lp.html`).
- Grid baseado em 12 col em desktop. Gap padrão 24px. Em conteúdo denso de LP: coluna única centralizada.

### Animação
- **Filosofia:** movimentos curtos, decisivos, "ease-out" agudo. Nada bouncy, nada lento.
- Durações: 120ms (interação) / 200ms (transição UI) / 400ms (entrada de seção).
- Easing padrão: `cubic-bezier(0.22, 1, 0.36, 1)`.
- Hover padrão: `filter: brightness(1.12)` em CTA; `border-color` dourado em cards; sem transformações de escala.
- Press: `transform: translateY(1px)` ou `filter: brightness(0.95)`. Nunca shrink >2%.
- Fades OK (200ms). Entradas decks: cortina preta de baixo, não "slide from right".

### Use de blur / transparência
- Glass blur apenas em **navbars sticky** em LP longa (`backdrop-filter: blur(12px)` com `rgba(0,0,0,0.6)`).
- Protection gradient: quando sobrepor texto em foto, usar gradient preto 85% → 0% vindo da borda do texto. Nunca caixa sólida atrás de texto sobre foto (mata o cinematográfico).

### Corner radii
| Uso | Radius |
|---|---|
| Chips / badges | `9999px` (pill) |
| Botões, inputs | 3px |
| Cards pequenos | 6px |
| Cards grandes / modais | 8px (teto) |
| Imagens hero | 0 (full-bleed) |

### Color vibe de imagery
- **Duas vertentes coexistem** (ver `assets/`):
  1. **Cinemática F1 / escritório:** alto contraste, sombras profundas, um único acento dourado ou amarelo cortando o preto (`brand-racing-suit-gold.png`, `brand-racing-white-yellow.png`).
  2. **Executivo retrato:** B&W ou sépia fria com skintones naturais (`airton-portrait.png`, `brand-coffee-study.png`).
- Nunca: fotos coloridas saturadas, fundos brancos de stock, lifestyle "tech bro" ensolarado.
- Grain leve (~4% noise) é OK em assets hero.

---

## Iconography

**A marca não possui um icon system proprietário.** Inventário do que foi encontrado:

- **Mascote / símbolo:** o **lobo de 3/4 de perfil** em traço monocromático (ver `assets/wolf-mark-light.png`). Representa "instinto, caça agressiva pela meta, inteligência de matilha". Aparece sozinho em situações onde o wordmark não cabe (favicon, watermark, selo).
- **Wordmark:** `SENA` em serifa display alta com subline `EXPANSÃO COMERCIAL` em caixa alta tracking largo (ver `assets/logo-sena-*.png`). Usado em versões clara (fundo escuro) e escura (fundo claro).
- **Unicode / emoji funcional** (observado no `mavis-lp.html` — este é o padrão estabelecido):
  - `✅` — bullets de benefício
  - `📲` — CTA WhatsApp / Meet
  - `📌` — proof / caso
  - `👇` — direcionamento de fluxo
  - `⚡` — aceitável como "ignição" em anúncios curtos
  - Números em círculo dourado/laranja — steps numerados (padrão `filter-block`)

### Substituição recomendada: **Lucide**
Para ícones de UI geral (arrow-right, check, x, menu, chart, etc.) que a marca **não tem** hoje, usar **[Lucide](https://lucide.dev)** via CDN:

```html
<script src="https://unpkg.com/lucide@latest/dist/umd/lucide.js"></script>
<i data-lucide="arrow-right"></i>
<script>lucide.createIcons();</script>
```

Stroke weight 2px combina com a sensação "telemetria fria" da marca. **⚠️ Flag:** isso é uma substituição sugerida — ainda não há validação do fundador. Pedir confirmação antes de publicar em produção.

### SVGs e PNGs
Todos os logos e o wolf mark estão em `assets/` como **PNG** (fonte original do brandbook). Se for necessário SVG escalável para hero, pedir ao usuário o arquivo vetorial.

---

## Caveats / flags

1. **Fontes não fornecidas como arquivos.** Brandbook cita Baskerville/Playfair (display) e Inter/Helvetica/Montserrat (corpo). Estamos usando **Playfair Display + Montserrat via Google Fonts** como substitutos fiéis. Se vocês tiverem um TTF específico licenciado, substituir.
2. **Icon system é improvisado.** Substituição: Lucide. Pedir validação.
3. **Logo vetorial.** Só recebemos PNGs do wordmark/lobo. Para escalonar sem perda, precisamos do SVG/AI.
4. **Copy master (MVM - Copy & Storytelling)** — não foi lido por limitação de path com caracteres especiais; extraímos tom de voz do Brandbook + LP existente. Se há termos canônicos adicionais, vale revisar.

---

## Index (este arquivo)

- **Tokens:** [`colors_and_type.css`](./colors_and_type.css)
- **UI kit principal:** [`ui_kits/mavis-landing/`](./ui_kits/mavis-landing/) — LP da Masterclass MaVIS recriada em componentes JSX
- **Slides de oferta:** [`slides/`](./slides/) — deck de oferta MaVIS (capa, mecanismo, metodologia, precificação)
- **Assets:** [`assets/`](./assets/)
- **Preview cards (Design System tab):** [`preview/`](./preview/)
- **Docs originais:** [`source_docs/`](./source_docs/)
- **Skill file:** [`SKILL.md`](./SKILL.md)
