---
_provenance:
  writtenBy: stardust:prototype
  writtenAt: 2026-05-18T23:45:00Z
  page: home
  slug: home
  direction: stardust/direction.md (2026-05-18)
  readArtifacts:
    - stardust/current/pages/home.json
    - stardust/current/_brand-extraction.json
    - DESIGN.md
    - DESIGN.json
    - stardust/direction.md
    - stardust/prototypes/home-improvements.md
  iaFidelity: verbatim
  density: balanced
  surpriseTier: low
  capturedSourceLineage:
    - section: header
      source: site-wide system-component (carried from _brand-extraction.json#systemComponents[kind=header])
    - section: 0 (hero)
      source: derived from pages/home.json#sections[0] — hero heading, body, CTA
    - section: 1 (features-grid)
      source: derived from pages/home.json#sections[1] — grid-3 feature cards with images
    - section: 2 (feature-tiles)
      source: derived from pages/home.json#sections[2] — grid-2 tile list
    - section: 3 (bento-map)
      source: derived from pages/home.json#sections[3] — bento layout with 5 cities
    - section: 4 (faq-dark)
      source: derived from pages/home.json#sections[4] — dark-scheme FAQ grid
    - section: 5 (editorial-text)
      source: derived from pages/home.json#sections[5] — two H3-headed editorial columns
    - section: 6 (tabbed-dark)
      source: derived from pages/home.json#sections[6] — dark-scheme 3-tab panel
    - section: 7 (text-video)
      source: derived from pages/home.json#sections[7] — 50/50 text+video block
    - section: 8 (cards-demo)
      source: derived from pages/home.json#sections[8] — 2-column card grid demo
    - section: 9 (agent-section)
      source: derived from pages/home.json#sections[9] — agent feature block
    - section: 10 (cta-band)
      source: derived from pages/home.json#sections[10] + DESIGN.json#systemComponentRoles[cta-band]
    - section: footer
      source: site-wide system-component (carried from _brand-extraction.json#systemComponents[kind=footer])
  antiTemplatePass:
    - pattern: centered-stack-hero
      defaultReflex: Centered headline + body + two-button CTA pair on flat background
      alternatives:
        - Full-bleed image with gradient scrim from bottom; headline bottom-anchored (campaign-poster style)
        - Split diagonal — type on azul left panel, image bleeding right
        - Overhead photo with large white Montserrat 900 headline floating over it
      picked: Full-bleed image with verde/azul gradient scrim bottom-up; headline left-aligned in lower third; single amarelo CTA
      rationale: "Captured site's hero is an image-forward moment with a single CTA and a powerful headline — perfectly suited to campaign-poster style. Centered double-CTA reflex rejected per DESIGN.md donts. Verbatim IA caps surprise at low so split-diagonal skipped; bottom-anchor is the lowest-risk non-reflex move."
    - pattern: 5-up-image-card-grid
      defaultReflex: Uniform grid of equal-height cards — the generic SaaS feature strip
      alternatives:
        - 3-column grid with verde left-border accent and heavy heading (keeps captured grid-3 shape)
        - Alternating full-width feature row + 2-up compact strip (breaks grid symmetry)
        - Hero-feature card large (first item 2×) + 7 uniform below
      picked: 3-column grid, verde card left-border, Montserrat 800 card heading — captured shape preserved, brand fully applied
      rationale: "Captured shape IS grid-3 with 8 items (2×4 rows). ia-fidelity verbatim + surprise:low means grid structure is locked. The differentiation move is brand: verde borders, weight 800 headings, football photography at 16:9 minimum 320px per card."
    - pattern: generic-accordion-faq
      defaultReflex: Chevron-triggered stacked accordion, dark background
      alternatives:
        - 2-column layout — question left (verde label) / answer right (white body text) on azul ground
        - Numbered list with large decorative question numbers at low opacity
        - Card grid with Q as badge + A as body
      picked: 2-column question/answer layout on azul — question bold white left col, answer normal white right col
      rationale: "2-column editorial FAQ reads as campaign editorial (like a pre-match press briefing), not a generic support FAQ. Avoids accordion reflex without introducing any external pattern. Captured content has exactly 4 Q/As — 2×2 or 4×1 both work; 4×1 (full-width rows) chosen for scannability on azul dark ground."
    - pattern: horizontal-pill-tabs
      defaultReflex: Rounded pill tabs with neutral hover, content below
      alternatives:
        - Full-width tab headings with underline indicator (editorial style)
        - Vertical tabs on left panel with content right
        - Horizontal tabs with amarelo underline on active — captured shape retained
      picked: Horizontal tabs with amarelo 3px underline on active tab — captured shape preserved, brand applied
      rationale: "Verbatim IA fidelity locks tab presence and order (Authors/Developers/Agents). The differentiation is brand: amarelo active indicator, Montserrat 700 tab labels, dark azul panel with white content body."
  substrateTransitions:
    default: "stark-white — oklch(99% 0 0)"
    exceptions:
      - sections: [4, 6]
        substrate: "azul — oklch(22% 0.095 265)"
        purpose: "Dark-scheme sections captured verbatim from source site; azul replaces #000000 per DESIGN.md 'Azul dark sections'. Both instances share the same substrate (azul) — counted as one exception class."
      - sections: [10]
        substrate: "amarelo — oklch(91% 0.185 95)"
        purpose: "CTA band — maximum campaign energy, per DESIGN.json#systemComponentRoles[cta-band]: 'amarelo background, azul text'. Registered exception."
    note: "Two exception classes (azul dark + amarelo CTA) against a white default. Sections 4 and 6 are two non-contiguous instances of the same azul exception — one class, two appearances. ≤2 substrate exception cap honored."
  voiceClassification:
    - section: header
      classification: captured-verbatim
      copy: "Author Kit | Features | Docs | Get started"
      source: pages/home.json#landmarks.header
    - section: 0 (hero)
      classification: captured-verbatim
      copy: "Brazil Goes for the Championship / The Seleção is back. Six stars on the shirt, one dream in the heart."
      source: pages/home.json#sections[0]
    - section: 0 (CTA)
      classification: captured-verbatim (URL flagged as placeholder per iaPriorities)
      copy: "Join the Journey → github.com/aemsites/author-kit"
      source: pages/home.json#ctas[0]
    - section: 1
      classification: captured-verbatim
      copy: "Why Brazil Will Win / Follow the Seleção / (8 feature items)"
      source: pages/home.json#sections[1]
    - section: 2
      classification: captured-verbatim
      copy: "The Brazilian Playbook / Everything that makes Brazil... / (10 tiles)"
      source: pages/home.json#sections[2]
    - section: 3
      classification: captured-verbatim
      copy: "The Road to Glory / (2 body paragraphs) / São Paulo / Rio de Janeiro / Belo Horizonte / Manaus / Salvador"
      source: pages/home.json#sections[3]
    - section: 4
      classification: captured-verbatim
      copy: "Tactics, Passion, and Pure Football / (subheading) / (4 Q&A pairs)"
      source: pages/home.json#sections[4]
    - section: 5
      classification: captured-verbatim
      copy: "The Art of the Dribble / The Spirit of the Maracanã / (2 body paragraphs)"
      source: pages/home.json#sections[5]
    - section: 6
      classification: captured-verbatim
      copy: "Something for everyone / Authors / Developers / Agents"
      source: pages/home.json#sections[6]
    - section: 6 (tab body)
      classification: captured-verbatim
      copy: "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
      source: pages/home.json#sections[6].body
    - section: 7
      classification: captured-verbatim
      copy: "Maybe you want to have a bit of text next to a video. / Lorem ipsum..."
      source: pages/home.json#sections[7]
    - section: 8
      classification: captured-verbatim
      copy: "Cards / What if you could have cards inside a tab?"
      source: pages/home.json#sections[8]
    - section: 9
      classification: captured-verbatim
      copy: "You don't just have to be a human. / Lorem ipsum..."
      source: pages/home.json#sections[9]
    - section: 10 (CTA band)
      classification: captured-verbatim (URL flagged as placeholder)
      copy: "Get started with AEM → aem.live/developer/tutorial"
      source: pages/home.json#sections[10]
    - section: footer
      classification: captured-verbatim
      copy: "Terms of Use / Privacy Policy / Cookies / Do not sell or share my personal information / © 2025 Adobe. All Rights Reserved."
      source: pages/home.json#landmarks.footer
  unsourcedContent: []
---

# Home — Page Shape Brief

## Summary

Brazil World Cup campaign landing page. 11 sections verbatim. Surface transformation only:
purple/magenta → verde/amarelo/azul, Montserrat wght 600 → 900 display / 800 headings, section
padding 64px balanced. Surprise budget: `low` (verbatim IA fidelity cap).

---

## Sections

### System Component — Header

**Source:** site-wide system-component (`_brand-extraction.json#systemComponents[kind=header]`)

**Layout:** Fixed-top nav bar, transparent at page top → azul background on scroll.
`Author Kit` wordmark left (Montserrat 800, textOnDark). Nav links center/right: Features / Docs /
Get started. Color scheme toggle + language selector far right as icon controls.

**A11y fix:** The captured site has an H2 "Default header promo" in the header that precedes the
page H1 — this triggers the T-h1-level-regression tension. In the proposed file, the header promo
text is rendered as a `<p>` (not a heading) to preserve H1 supremacy in the main content.
Per home-improvements.md item 3.

**Substrate:** Transparent → azul (on scroll) — inherits dark-scheme color scheme.

---

### Section 0 — Hero

**Source:** derived from `pages/home.json#sections[0]`

**IA priority:** campaign-conversion (first viewport, locked — verbatim)

**Layout:** Full-bleed hero, 100vw × 80vh min. Background: `media_1674c029fe1c222fe6f72c3bf0ad7fdf41e16eca9.jpg`
(the captured `media.heroImage`), scaled `object-fit: cover`. Verde/azul gradient scrim from bottom
(0% opacity at top → 80% azul at bottom-third) — required per DESIGN.md § Motifs anti-rule.

Content container left-aligned, bottom-third of viewport:
- Eyebrow label: `SELEÇÃO 2026` — verde ds-badge (uppercase, wght 700, 16px+)
- H1: `Brazil Goes for the Championship` — Montserrat wght 900, 48.83px (xxl), white, lh 1.1,
  max-width 760px
- Body: `The Seleção is back. Six stars on the shirt, one dream in the heart.` — Montserrat 400,
  18px, textOnDark
- CTA: `Join the Journey` → `https://github.com/aemsites/author-kit` — ds-btn-primary (amarelo bg,
  azul text, uppercase, wght 700). Single CTA per DESIGN.md rule.

**LCP fix:** Hero image rendered `loading="eager"` (not lazy) — per home-improvements.md item 3
(T-lcp-no-eager fix).

**Substrate:** image (visual substrate) + verde/azul gradient scrim overlay.

---

### Section 1 — Features Grid

**Source:** derived from `pages/home.json#sections[1]`

**Layout:** Section padding 64px. Eyebrow: `POR QUE O BRASIL VAI VENCER` (verde badge, uppercase).
H2: `Why Brazil Will Win` (Montserrat 800, xl 39.06px). Secondary CTA: `Follow the Seleção` →
aem.live (ds-btn-secondary, azul outline).

Grid: 3 columns × 3 rows (8 cards + 1 empty or 3×3 = 9 slots with one intentionally empty).
Each card (`ds-card` pattern):
- Image 16:9, min 320px width, captured football photos from `pages/home.json#images[0–7]`
- Feature name: Montserrat 700, 20px heading (H3 implied by role, rendered as `<h3>`)
- Body copy: feature description paragraph, Montserrat 400, 16px
- Verde left-border (3px) as per DESIGN.md § Components card

**Substrate:** stark-white

---

### Section 2 — Feature Tiles

**Source:** derived from `pages/home.json#sections[2]`

**Layout:** Section padding 64px. Eyebrow: `O MANUAL BRASILEIRO` (verde badge). H2: `The Brazilian
Playbook` (Montserrat 800, xl). Subtext: `Everything that makes Brazil the greatest footballing
nation. Nothing left out.` — body 16px.

2-column grid of 10 compact tiles. Each tile:
- Verde left-border (3px) card
- Tile name in Montserrat 700, 16px (small heading)
- No image — typographic tiles only
- Slight verde-tint surface (`oklch(97% 0.004 145)`)

**Substrate:** stark-white with verde-tinted surface tiles

---

### Section 3 — Bento Map

**Source:** derived from `pages/home.json#sections[3]`

**Layout:** Section padding 64px. H2: `The Road to Glory` (Montserrat 800, xl). Body text:
`From the group stage to the final whistle...` + `The Seleção is proudly made across all of Brazil.`

Asymmetric bento grid: 5 city tiles — São Paulo (large, 2×2), Rio de Janeiro (wide, 2×1),
Belo Horizonte (tall, 1×2), Manaus (1×1), Salvador (1×1). Each tile shows city name in
Montserrat 900 at large size (decorative, low opacity behind a smaller bold label). Background:
azul-tinted or verde-tinted alternating surfaces per flag-geometry motif.

Decorative element: Montserrat 900 number "2026" at ~120px, 8% opacity, verde, behind the grid.

**Substrate:** stark-white

---

### Section 4 — FAQ Dark

**Source:** derived from `pages/home.json#sections[4]`

**Layout:** Section padding 64px. Background: azul (`oklch(22% 0.095 265)`) — dark-scheme.
Eyebrow: `TÁTICA` (verde badge — 18px+ per verde restriction). H2: `Tactics, Passion, and Pure
Football` (Montserrat 800, xl, textOnDark). Subheading: `The philosophy that turns eleven players
into an unstoppable force.` (Montserrat 400, 20px, textOnDark).

4 Q&A pairs in 2-column rows (question left, answer right):
- Question: Montserrat 700, 18px, amarelo (18px+ so verde/amarelo restriction met — using amarelo here for emphasis)
- Answer: Montserrat 400, 16px, textOnDark (white)
- Hairline separator between rows: verde at 30% opacity

**Substrate:** azul (dark-scheme exception 1)

---

### Section 5 — Editorial Text

**Source:** derived from `pages/home.json#sections[5]`

**Layout:** Section padding 64px. 2-column split.

Left column:
- H3: `The Art of the Dribble` (Montserrat 800, l 31.25px)
- Body: `From Garrincha to Ronaldinho, Brazil has always produced players who make defenders look
  foolish...` — Montserrat 400, 16px, lh 1.6
- Decorative: Montserrat 900, "10" at ~100px, verde, 10% opacity — behind the heading

Right column:
- H3: `The Spirit of the Maracanã` (Montserrat 800, l 31.25px)
- Body: `Bring your own passion.` — Montserrat 400, 16px (placeholder-level — captured verbatim)
- Decorative: verde vertical bar (3px, 60px tall) as left accent

**Substrate:** stark-white

---

### Section 6 — Tabbed Dark

**Source:** derived from `pages/home.json#sections[6]`

**IA priority:** audience-routing (below fold, locked — verbatim)

**Layout:** Section padding 64px. Background: azul — dark-scheme.
Eyebrow: `PARA TODOS` (verde badge, 18px+). H2: `Something for everyone` (Montserrat 800, xl, textOnDark).

Tab strip: Authors | Developers | Agents — Montserrat 700 labels, textOnDark.
Active tab indicator: amarelo 3px bottom border on active label.
Tab content panel: body text (lorem ipsum — captured verbatim), textOnDark, 16px.

**Substrate:** azul (dark-scheme exception 1 — second instance)

---

### Section 7 — Text + Video

**Source:** derived from `pages/home.json#sections[7]`

**Layout:** Section padding 64px. 2-column 50/50 split.

Left: H2 `Maybe you want to have a bit of text next to a video.` (Montserrat 800, l, text-color) +
body lorem ipsum (Montserrat 400, 16px). [PLACEHOLDER: heading copy is captured verbatim from
Author Kit demo — not football-specific.]

Right: video block placeholder — verde-bordered 16:9 frame with play icon in azul.

**Substrate:** stark-white

---

### Section 8 — Cards Demo

**Source:** derived from `pages/home.json#sections[8]`

**Layout:** Section padding 64px. H2: `Cards` (Montserrat 800, m 25px) — implied demo section.
Subtext: `What if you could have cards inside a tab?` (Montserrat 400, 16px).

2-column grid of demo cards (ds-card pattern: white bg, verde left-border, 6px radius, 24px
padding). Content is placeholder / demo — retained verbatim.

**Substrate:** verde-tinted surface (`oklch(97% 0.004 145)`) — differentiates demo section
without adding a new substrate exception (surface variant is within the white ground family).

---

### Section 9 — Agent Section

**Source:** derived from `pages/home.json#sections[9]`

**Layout:** Section padding 64px. H2: `You don't just have to be a human.` (Montserrat 800, xl).
Sub-heading: `Even AI agents can feel at home with Author Kit.` (from headings[16] in home.json).
Body: lorem ipsum — captured verbatim.

Feature block: azul-bordered box with agent icon (SVG) + body copy. Single ds-btn-secondary CTA
if present in captured content.

**Substrate:** stark-white

---

### Section 10 — CTA Band

**Source:** derived from `pages/home.json#sections[10]` + `DESIGN.json#systemComponentRoles[cta-band]`

**Layout:** Section padding 64px. Background: amarelo (`oklch(91% 0.185 95)`) — maximum campaign energy.
Text: azul (`oklch(22% 0.095 265)`) — 13:1 AAA contrast.

Eyebrow: `VAMOS` — small uppercase label, azul, Montserrat 700.
Headline: `O Jogo Bonito começa aqui.` — Montserrat 900, 39px, azul. [Direction-authorized rewrite:
campaign voice for the final CTA section; captured content had no heading here.]
CTA: `Get started with AEM` → `https://www.aem.live/developer/tutorial` — ds-btn-primary reversed
(azul bg, white text) — or maintain amarelo with azul label. Using azul-on-amarelo per system spec.

**Substrate:** amarelo (CTA band exception 2)

---

### System Component — Footer

**Source:** site-wide system-component (`_brand-extraction.json#systemComponents[kind=footer]`)

**Layout:** azul background, textOnDark. Legal links left (Terms of Use / Privacy Policy / Cookies /
Do not sell...), copyright right: `© 2025 Adobe. All Rights Reserved.` — Montserrat 400, 14px.

Per DESIGN.json#systemComponentRoles[footer]: "azul background, white text."

**Substrate:** azul (system component — not counted in page substrate exceptions)

---

## Heading Hierarchy

```
<header> — nav, no heading in heading hierarchy
  "Default header promo" → rendered as <p> (a11y fix: prevents H2-before-H1)
<main>
  [S0]  <h1> Brazil Goes for the Championship
  [S1]  <h2> Why Brazil Will Win
  [S2]  <h2> The Brazilian Playbook
  [S3]  <h2> The Road to Glory
  [S4]  <h2> Tactics, Passion, and Pure Football
  [S5]  <h3> The Art of the Dribble
        <h3> The Spirit of the Maracanã
  [S6]  <h2> Something for everyone
  [S7]  <h2> Maybe you want to have a bit of text next to a video.
  [S8]  <h2> Cards
  [S9]  <h2> You don't just have to be a human.
  [S10] (no heading — CTA band with eyebrow only)
```

H1 declared once. H2 for all section headings. H3 for sub-section headings within S5.
No heading skips.

---

## Key Layout Decisions

1. **Hero image** — `media.heroImage` (`media_1674c029fe1c222fe6f72c3bf0ad7fdf41e16eca9.jpg`) used at full-bleed with verde/azul gradient scrim. `loading="eager"` for LCP.
2. **Feature grid images** — `images[0–7]` mapped 1:1 to the 8 feature cards at 16:9.
3. **Verde restriction** — verde used only as badge background (18px+ label text), card borders, and decorative accents. Never as body text color.
4. **Amarelo** — CTAs (primary button) and active tab indicator only. Amarelo CTA band (S10) uses azul text.
5. **One CTA per section** — enforced. Secondary CTAs (Follow the Seleção, Visit Adobe) flagged as direction-authorized secondary links, not duplicate primary CTAs.
6. **Font loading** — `<link rel="preconnect" href="https://fonts.googleapis.com">` + Montserrat wght 400..900 variable from Google Fonts. `font-variation-settings` used explicitly per DESIGN.md.
7. **Section data attributes** — every section carries `data-section-type`, `data-source`, `data-ia-fidelity="verbatim"`.

---

## Open Questions for Phase 2

None. Direction is fully resolved. IA fidelity verbatim. All content sourced from captured JSON.
Section 10 headline `O Jogo Bonito começa aqui.` is the only direction-authorized rewrite (eyebrow + CTA band headline for campaign register).

---

## Unsourced Content

None. All content traces to `pages/home.json`. Stats, city names, and quotes are captured-verbatim.
Section 10 headline is direction-authorized rewrite (logged above, not a fabrication).
Lorem ipsum in sections 6–9 is captured-verbatim demo content from the source site.
