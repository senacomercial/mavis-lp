# SKILL — Sena Comercial Design System

When designing anything for **Sena Comercial** (landing pages, decks, emails, ads, dashboards, internal docs) in this project or a copy of it, follow these rules. This is a Claude Code-compatible skill file that complements `README.md`.

## 1. Read before you design
- **Always** start by reading `README.md` (full context, tone, palette, caveats).
- If the task is typography- or color-heavy, skim `colors_and_type.css` — use the CSS variables, do not invent hex codes.
- For visual references, the source of truth is `source_docs/mavis-lp.html` (implemented UI) and `source_docs/Brandbook Sena.pdf` (strategy + identity). `ui_kits/mavis-landing/` is the working recreation.

## 2. Positioning (never forget)
- Sena is an **escuderia de estruturação comercial** — F1 paddock metaphor, not a generic "marketing agency".
- Hero archetype + Governante/Rebelde traits. Zero enrolação, verdade bruta, precisão cirúrgica.
- The word we own: **ESTRUTURAÇÃO / RESULTADO-CRU**.
- Flagship product: **MaVIS** — Máquina de Vendas Imobiliárias da Sena.
- Primary audience: founders of imobiliárias, construtoras, incorporadoras and other PMEs. Secondary: autonomous corretores.

## 3. Non-negotiables (visual)
1. **Default background is `#000`**. Light/cream is for print only or as an accent.
2. **Playfair Display italic + laranja (`#E85D04`) or dourado (`#C5A059`)** is the signature highlight inside a sans-serif headline. Every hero needs one. Italic means "velocidade e grife".
3. **One accent at a time.** Gold = pódio/prestígio. Orange = ignição/action. Don't mix both screaming in the same viewport.
4. **Sharp corners.** Radii cap at 8px for cards, 3px for buttons. Pills only for chips/badges. Never 24px+ rounded corners.
5. **No gradient backgrounds** beyond the two permitted ones (subtle vertical black fade, radial orange "faísca"). No blue/purple. No rainbow.
6. **Telemetria typography** — numbers and critical metrics go in `JetBrains Mono`, tabular numerics, gold/orange color. Never a serif number.
7. **Filter-block is the signature component:** 3px orange left-border on a 6% orange-tinted surface with numbered circle steps. Use it for any "protocol/process" content.
8. **No fake imagery.** Use the provided photos in `/assets/`. If a scene doesn't exist, leave a grey placeholder and flag it — never generate AI slop F1 scenes.

## 4. Non-negotiables (copy)
- Portuguese BR. Keep marketing jargon in English only when consecrated (lead, CPL, closer, pipeline, ticket, CRM).
- Proprietary terms in **Playfair italic**: *Filtro de Intencionalidade Pós-Clique*, *Lead Inerte*, *Sequestro de Atenção*, *Montanha-Russa Financeira*, *Pedágio Obrigatório*.
- Second person (você). Never "nós" vago.
- Numbers > adjectives. "R$ 300 → R$ 1.000.000" beats "resultado extraordinário".
- UPPERCASE only for CTAs, urgency banners ("NA PRÓXIMA TERÇA — 12H"), and overlines.
- Emoji strictly functional: `✅ 📲 📌 👇 ⚡` — never decorative (🎉✨🚀💎🔥 prohibited).

## 5. When you need a component
Before writing from scratch, check these (in order):
1. `ui_kits/mavis-landing/*.jsx` — React components (Nav, Hero, FilterBlock, ProofStrip, UrgencyBadge, MetricCard, PricingCard, SectionHeader, CTAButton, Footer).
2. `preview/` — isolated demo cards for every pattern.
3. `colors_and_type.css` — tokens + base classes (`.sena-display`, `.sena-overline`, `.sena-highlight`, `.sena-metric`).

## 6. Slide decks
Start from `slides/index.html` as the canonical template. It uses `<deck-stage>` — every new slide is a direct-child `<section>` with `data-label`. The visual system (black bg, serifa headlines with italic orange/gold highlight, JetBrains Mono metrics, filter-block, pricing cards, footer with slide number) is already wired. Do not re-skin.

## 7. What to do when resources are missing
- **Need an icon?** Use Lucide via CDN (already set up in `preview/iconography.html`). Stroke 2px.
- **Need a vectored logo?** Ask the user — we only have PNGs.
- **Need a specific font file?** We use Google Fonts (Playfair + Montserrat + JetBrains Mono) as substitutes for the brandbook's Baskerville/Inter. If the user has licensed files, swap via `@font-face`.
- **Unsure of copy tone?** Re-read "Voice & Tone" in README.md and `preview/voice-do-dont.html`.

## 8. Flags to always disclose
- Font substitution (Playfair ≠ Baskerville literally, but same family spirit).
- Icon system is improvised (Lucide).
- Logo is raster only.
- Copy master (`MVM - Copy & Storytelling Master Document`) was not fully ingested — verify any new canonical terms against the user.

## 9. Output discipline
- No filler sections. No "sobre nós" unless asked. No lorem ipsum.
- Prefer 3 tight pages over 8 padded ones.
- Every CTA must tie to one of: `Agendar diagnóstico`, `Entrar no Grupo VIP`, `Ver cronograma`, `Conversar com a Sena`.
