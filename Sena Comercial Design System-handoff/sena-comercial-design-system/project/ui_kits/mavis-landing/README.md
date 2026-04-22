# UI Kit — MaVIS Landing / Sena Site

Recreation of the **MaVIS Masterclass** landing page (source: `/source_docs/mavis-lp.html`), extended into a full Sena Comercial site mock with the canonical components.

## Components

- `Nav.jsx` — sticky top bar with wolf mark + wordmark, nav links, primary CTA
- `Hero.jsx` — full-bleed black hero with serifa italic highlight headline pattern
- `FilterBlock.jsx` — orange-accent 3-step protocol (THE signature component from the brandbook/LP)
- `ProofStrip.jsx` — 📌 case studies with gold strong-text
- `UrgencyBadge.jsx` — red CAPS urgency block
- `CTAButton.jsx` — gold primary, ignition secondary
- `MetricCard.jsx` — telemetry-style number card (mono font, gold/orange accent)
- `BulletList.jsx` — ✅ and numbered variants
- `SectionHeader.jsx` — overline + serifa display title pattern
- `Footer.jsx`

## Running
Open `index.html` directly — uses inline Babel/React UMD, loads `../../colors_and_type.css`.

The demo shows a full single-page mock: Nav → Hero → Mechanism → Method (FilterBlock) → Proof → Pricing → CTA → Footer. Click-through limited: clicking the primary CTA scrolls to the filter section (prototype).

## Source of truth
Visuals lifted directly from `mavis-lp.html` (colors, spacing, type stack). Any deviation is documented inline with `{/* lifted-from-mavis-lp */}` comments.
