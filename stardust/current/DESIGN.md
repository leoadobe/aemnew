---
colors:
  background: "#ffffff"
  surface: "#f9f9f9"
  text: "#1b1b1b"
  brand: "#9d60d8"
  accent: "#bd0084"
  dark: "#000000"
  textOnDark: "#ffffff"
typography:
  headingFamily: "Montserrat"
  bodyFamily: "Montserrat"
  headingWeight: 600
  bodyWeight: 400
  baseSize: "16px"
  scaleRatio: 1.122
  headingSizes:
    xxl: "32.44px"
    xl: "28.83px"
    l: "25.63px"
    m: "22.78px"
    s: "20.25px"
    xs: "18px"
  lineHeightHeading: 1.15
  lineHeightBody: 1.6
rounded:
  primary: "4px"
  note: "Not explicitly set in captured tokens; small radius inferred from brand register"
spacing:
  base: "4px"
  xs: "4px"
  s: "8px"
  m: "12px"
  l: "24px"
  xl: "32px"
  xxl: "48px"
  sectionPadding:
    desktop: "48px"
    tablet: "36px"
    mobile: "24px"
components:
  button-primary:
    background: "#bd0084"
    color: "#ffffff"
    class: "btn btn-accent"
    radius: "4px"
  button-secondary:
    background: "transparent"
    color: "#1b1b1b"
    border: "1px solid #1b1b1b"
  card:
    background: "#ffffff"
    radius: "4px"
    shadow: "none"
  link:
    color: "#1b1b1b"
    underline: "on hover"
_provenance:
  writtenBy: stardust:extract
  writtenAt: 2026-05-18T23:16:26.664Z
  readArtifacts:
    - stardust/current/_brand-extraction.json
    - stardust/current/pages/home.json
  note: Descriptive snapshot of the existing design system — not the redesign target.
---

# DESIGN.md — Current State (Descriptive)

## Overview

The Author Kit site uses a single-family type system (Montserrat variable font, wght 100–900)
with a purple brand color and magenta accent. The palette is systematically defined across 9 color
scales (gray, green, teal, blue, purple, magenta, red, orange, yellow) plus semantic roles.
The site supports light/dark mode via CSS `light-dark()`.

The Brazil World Cup demo theme lays energetic editorial content — football photography, bold
headlines, and vivid section variety — on top of the Author Kit component system.

## Colors

**Semantic roles** (from CSS custom properties):

| Role | Light | Dark | Source |
|---|---|---|---|
| `--color-background` | `#ffffff` | `#000000` | `light-dark()` |
| `--color-shaded` | `#f9f9f9` | `#111111` | `light-dark()` |
| `--color-text` | `#000000` | `#ffffff` | `light-dark()` |
| `--color-link` | `#1b1b1b` | `#f1f1f1` | `light-dark()` |
| `--color-brand` | `#9d60d8` | `#9d60d8` | `--color-purple-500` |
| `--color-accent` | `#bd0084` | `#eb00a5` | `--color-magenta-600/500` |

**Color scales**: Gray (100–900), Purple (100–900), Magenta (100–900), plus Green, Teal, Blue,
Red, Orange, Yellow — full 9-step scales each.

## Typography

Single variable font: **Montserrat** (Google Fonts, OFL licensed), wght 100–900, normal + italic.
Fallback: `"Trebuchet MS", sans-serif`.

Heading scale (~1.122 ratio, modular):
- H1 / `--heading-font-size-xxl`: 32.44px / weight 600
- H2 / `--heading-font-size-xl`: 28.83px / weight 600
- H3 / `--heading-font-size-l`: 25.63px
- H4 / `--heading-font-size-m`: 22.78px
- H5 / `--heading-font-size-s`: 20.25px
- H6 / `--heading-font-size-xs`: 18px

Body base: 16px / line-height 1.6. Body scale runs xs–xxxl (12px–25px).

## Spacing

4px base grid. Section padding: `--spacing-xxl` (48px) on desktop.

Grid: 83.4% container width, 12-column system, 8.3% gutters. Section utilities:
`grid-2`, `grid-3`, `grid-4`, `layout-bento`, `container-6`.

## Motifs

- **Photography**: Bold, full-bleed football photography (action shots, team celebrations).
  Images are 1600px+ wide, delivered via AEM CDN with automatic optimization.
- **Section variety**: Dark-scheme sections alternate with light sections for visual rhythm.
- **SVG icons**: 9 SVG icons used in the feature-tiles section.
- **Bento grid**: Used for the "Road to Glory" cities section.

## Components

**Buttons**: `.btn.btn-accent` — magenta (`#bd0084`) background, white text. Used for all primary
CTAs: "Join the Journey", "Follow the Seleção", "Get started with AEM".

**Cards**: Image + heading + body in grid layouts (2, 3, or 4 columns depending on section).

**Tabs**: "Something for everyone" section uses Authors / Developers / Agents tabs with dark
background.

**FAQ/Accordion**: Dark-scheme grid-4 section for "Tactics, Passion, and Pure Football".

## Voice samples

- DO: Bold aspirational statements — "Six stars on the shirt, one dream in the heart."
- DO: Second-person empowerment — "Join the Journey", "Follow the Seleção"
- DO: Capability-confident — "Brazil's midfield can do both, adapting to any opponent's weak points."
- DON'T: Passive or hedged language.
- DON'T: Corporate-generic phrasing.
