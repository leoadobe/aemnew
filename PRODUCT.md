<!--
_provenance:
  writtenBy: stardust:direct
  writtenAt: 2026-05-18T23:30:00Z
  readArtifacts:
    - stardust/current/PRODUCT.md
    - stardust/current/_brand-extraction.json
    - stardust/current/pages/home.json
  stardustVersion: 0.7.1
-->

# PRODUCT.md — Target

## Register

Sports campaign, brand-flavored. The page is a World Cup campaign surface — its emotional register
is national pride and football passion, not product documentation. The underlying product (Author
Kit / AEM EDS) is showcased through the campaign content, not despite it.

## Users

**Primary:** Brazilian football fans and World Cup enthusiasts who encounter this page through
the 2026 World Cup campaign. They feel the Seleção's journey personally — they want to see
Brazil's colors, hear Brazil's voice, and feel the energy of a team that has won five titles
and is chasing a sixth.

**Secondary:** AEM developers and content authors discovering Author Kit through the demo —
they see a sophisticated, high-performance EDS site and recognize the toolkit's capability.

## Product Purpose

Author Kit demonstrates what AEM Edge Delivery Services can do — by doing it at World Cup
scale. A fast, richly-authored, visually bold campaign site that loads in milliseconds and
expresses the full emotional range of Brazilian football.

Scope: single landing page, World Cup / Seleção campaign, demonstrated on the Author Kit
block system.

## Brand Personality

**Bold, passionate, nationally proud.** The Seleção doesn't play cautiously — neither does
this design. Every weight is heavy, every color is saturated, every section has the energy
of a crowd singing the Brazilian national anthem.

**Warmth and joy.** Brazilian football is called "Jogo Bonito" — the beautiful game. The
design is not aggressive or brutal; it is joyful, expressive, and human.

**Technical confidence.** Under the campaign surface, the Author Kit architecture is
visible to developers who look for it — clean block structure, fast loading, responsive
from 375px up.

## Anti-references

- **Generic 2019 SaaS template** — centered hero, double CTA in matching teal, stock
  photography strip below. The purple/magenta palette we are replacing was drifting here.
- **Corporate sports sponsorship aesthetic** — navy + red + sans-serif corporate lockup.
  Brazil is not a sponsor; Brazil *is* the story.
- **Score-ticker / data-overlay sports UI** — stats panels, live score widgets, dark
  backgrounds with neon accents. This page is a celebration, not a broadcast.
- **Gradient text** — a hard rule violation; also inconsistent with the bold,
  flat Brazilian flag aesthetic.
- **Glassmorphism** — frosted-glass cards read as tech demo, not football passion.

## Design Principles

1. **Wear the colors.** Verde, amarelo, azul — every section earns its color from the
   Brazilian national palette. No other hues introduced.
2. **Type at full weight.** Montserrat at 900 for display; the font's variable range
   is a gift — use it.
3. **Photography is the emotion.** Football images are the page's heartbeat. Give them
   space, width, and respect — no thumbnail treatment for 1600px action shots.
4. **One CTA per section.** The Brazilian audience does not need four verbs meaning
   "engage." One clear call, one action, one conversion path per section.
5. **Verbatim structure, transformed surface.** The 11-section IA is kept intact —
   every section gets the Brazilian treatment, none get dropped or reordered.

## Accessibility & Inclusion

Language: `pt-BR` target audience (content is in English; future migration may localize).
WCAG AA required throughout: amarelo CTAs use azul text (13:1), dark sections use branco
text on azul ground (13.5:1), verde used only for large text and decorative surfaces (3.1:1).
Dark/light mode: inherited system support; campaign dark sections explicit via class.
