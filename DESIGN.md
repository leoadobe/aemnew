---
colors:
  background: "oklch(99% 0 0)"
  verde: "oklch(57% 0.165 145)"
  amarelo: "oklch(91% 0.185 95)"
  azul: "oklch(22% 0.095 265)"
  text: "oklch(18% 0 0)"
  textOnDark: "oklch(99% 0 0)"
  surface: "oklch(97% 0.004 145)"
typography:
  headingFamily: "Montserrat"
  bodyFamily: "Montserrat"
  displayWeight: 900
  headingWeight: 800
  bodyWeight: 400
  baseSize: "16px"
  scaleRatio: 1.25
  headingSizes:
    xxl: "48.83px"
    xl: "39.06px"
    l: "31.25px"
    m: "25px"
    s: "20px"
    xs: "16px"
  lineHeightHeading: 1.1
  lineHeightBody: 1.6
rounded:
  primary: "4px"
  card: "6px"
spacing:
  base: "4px"
  xs: "4px"
  s: "8px"
  m: "12px"
  l: "24px"
  xl: "32px"
  xxl: "64px"
  sectionPadding:
    desktop: "64px"
    tablet: "48px"
    mobile: "32px"
components:
  button-primary:
    background: "oklch(91% 0.185 95)"
    color: "oklch(22% 0.095 265)"
    borderRadius: "4px"
    fontWeight: 700
    html: '<a href="#" class="ds-btn ds-btn-primary">Junte-se à Jornada</a>'
  button-secondary:
    background: "transparent"
    color: "oklch(22% 0.095 265)"
    border: "2px solid oklch(22% 0.095 265)"
    borderRadius: "4px"
    fontWeight: 700
  card:
    background: "oklch(99% 0 0)"
    borderLeft: "3px solid oklch(57% 0.165 145)"
    borderRadius: "6px"
  badge:
    background: "oklch(57% 0.165 145)"
    color: "oklch(99% 0 0)"
    borderRadius: "4px"
  link:
    color: "oklch(22% 0.095 265)"
    underline: "on hover"
_provenance:
  writtenBy: stardust:direct
  writtenAt: 2026-05-18T23:30:00Z
  mode: targeted-palette-rebrand
  iaFidelity: verbatim
  density: balanced
  stardustVersion: 0.7.1
---

# DESIGN.md — Target (Brazil World Cup)

## Overview

A bold sports-campaign visual system built on the Brazilian national palette — verde, amarelo,
azul — applied to the Author Kit single-page demo. Montserrat variable font engaged at full
expressive weight (900 display, 800 headings). Section padding at 64px balanced tier. Verbatim
IA: same 11 sections transformed surface-only.

The design inherits the existing light/dark mode infrastructure and replaces every
purple/magenta token with a national color counterpart.

Seed: `2025-now × sports campaign × CBF kit tradition × stark-white ground`.

## Colors

**Palette — Brazilian national colors (OKLCH):**

| Role | OKLCH | Hex approx. | Use |
|---|---|---|---|
| `verde` | `oklch(57% 0.165 145)` | `#009C3B` | Brand, borders, decorative accents, large-text surfaces |
| `amarelo` | `oklch(91% 0.185 95)` | `#FFDF00` | CTAs, highlights, active states — always paired with azul text |
| `azul` | `oklch(22% 0.095 265)` | `#002776` | Dark sections, deep text, CTA text on amarelo |
| `background` | `oklch(99% 0 0)` | `#fefefe` | Page ground — near-white, not pure white |
| `surface` | `oklch(97% 0.004 145)` | `#f4faf5` | Subtle green-tinted section surface |
| `text` | `oklch(18% 0 0)` | `#1a1a1a` | Body text on light ground |
| `textOnDark` | `oklch(99% 0 0)` | `#fefefe` | Text on azul / verde dark sections |

**Contrast audit:**
- Azul text on amarelo CTA: ~13:1 — AAA ✓
- White on azul section: ~13.5:1 — AAA ✓
- Verde on white surface (decorative/large text only): ~3.1:1 — large-text AA ✓
- Body text (`#1a1a1a`) on white: ~18:1 — AAA ✓

**Verde restricted to large text / decorative use only.** Verde (`#009C3B`) at 3.1:1 fails WCAG AA
for body text. Use it for: section borders, eyebrow labels at 18px+ bold, card accents, icon fills,
and as a background surface for large white-text headlines. Never as body text color.

**Dark sections** use `azul` (`oklch(22% 0.095 265)`) as background with `textOnDark` foreground.
This replaces the existing `dark-scheme` / `#000000` pattern — azul is as dark and more
distinctly Brazilian.

## Typography

**Single variable family: Montserrat** (Google Fonts, OFL, wght 100–900).
Engaging the full weight range — this is the key expressive move from the current site.

Scale ratio: **1.25** (committed tier — up from 1.122).

| Level | Size | Weight | Use |
|---|---|---|---|
| Display / H1 | 48.83px | **900** | Hero headline — full campaign energy |
| H2 | 39.06px | **800** | Section headings |
| H3 | 31.25px | 700 | Sub-section headings |
| H4 | 25px | 700 | Card headings, feature labels |
| H5 | 20px | 600 | Eyebrow labels (uppercase) |
| Body | 16px | 400 | Paragraph text, lh 1.6 |
| Small | 14px | 400 | Captions, meta |

**Variable axis engagement:** `font-variation-settings: "wght" 900` on display elements.
Use `font-variation-settings` explicitly — do not rely on `font-weight: 900` alone.

**Heading line-height:** 1.1 (tight, campaign-poster feel at large sizes).
**Body line-height:** 1.6 (comfortable reading).

**Voice rule:** Mixed-case headings for all headings ≥ 3 words. Uppercase only for eyebrow
labels ≤ 3 words (e.g. "JOGO BONITO", "5× CAMPEÕES") and CTA button labels.

## Spacing

4pt base grid. Section padding: **64px desktop / 48px tablet / 32px mobile** (balanced tier,
hard floor honored — 11 sections on the page).

Grid: inherited 83.4% container width, 12-column. Unchanged.

Section gap tokens: `--spacing-xxl: 64px` replaces current `48px`.

## Motifs

**Full-bleed photography.** Football images at 1600px+ source width rendered at full container
width (100vw hero, min 480px card images at 16:9). Verde/azul gradient scrim on images with
text overlays — never raw text on photography.

**Brazilian flag geometry.** Verde borders (3px left) on light-surface cards. Amarelo used as
a horizontal rule / divider between sections. The three colors always appear in their canonical
hierarchy: verde as ground, amarelo as accent, azul as depth.

**Heavy type as decoration.** Montserrat 900 at large sizes (80px+) used decoratively behind
content — stats, city names, section numbers — in verde or amarelo at low opacity.

**Azul dark sections.** Replaces the existing `#000000` dark scheme. Every section that was
previously black becomes azul. The texture is warmer, distinctly national.

## Components

**`ds-btn-primary`** — amarelo background + azul text + wght 700. No gradient, no shadow.
The most Brazilian CTA possible: bold, flat, high-contrast.

```html
<a href="#" class="ds-btn ds-btn-primary">Junte-se à Jornada</a>
```

```css
.ds-btn-primary {
  background: oklch(91% 0.185 95);
  color: oklch(22% 0.095 265);
  font-family: Montserrat, "Trebuchet MS", sans-serif;
  font-variation-settings: "wght" 700;
  font-size: 1rem;
  padding: 12px 28px;
  border-radius: 4px;
  text-decoration: none;
  display: inline-block;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}
.ds-btn-primary:hover {
  background: oklch(85% 0.185 95);
}
```

**`ds-btn-secondary`** — azul outline + azul text. For secondary actions on light surfaces.

```css
.ds-btn-secondary {
  background: transparent;
  color: oklch(22% 0.095 265);
  border: 2px solid oklch(22% 0.095 265);
  font-variation-settings: "wght" 700;
  padding: 10px 26px;
  border-radius: 4px;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}
```

**`ds-card`** — white background, 3px verde left border, 6px radius.

```css
.ds-card {
  background: oklch(99% 0 0);
  border-left: 3px solid oklch(57% 0.165 145);
  border-radius: 6px;
  padding: 24px;
}
```

**`ds-badge`** — verde background, white text. Used for feature labels and section eyebrows.

```css
.ds-badge {
  background: oklch(57% 0.165 145);
  color: oklch(99% 0 0);
  font-variation-settings: "wght" 700;
  font-size: 0.75rem;
  padding: 4px 10px;
  border-radius: 4px;
  text-transform: uppercase;
  letter-spacing: 0.08em;
}
```

## Voice

**DO:**
- Bold declarative headlines: "Brazil Goes for the Championship"
- National pride without jingoism: "Seis estrelas no peito, um sonho no coração"
- Active, muscular verbs: "Join", "Follow", "Witness", "Feel"
- Short, punchy section openers that read like chants

**DON'T:**
- Corporate hedging: "solutions", "leverage", "synergy"
- Score-ticker overlay language: "LIVE · 2' · 1-0"
- Editorial-register vocabulary for what is a campaign: "the atelier", "the craft"
- More than one CTA per section
