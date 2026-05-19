---
_provenance:
  writtenBy: stardust:extract
  writtenAt: 2026-05-18T23:16:26.664Z
  readArtifacts:
    - stardust/current/_brand-extraction.json
    - stardust/current/pages/home.json
  note: Descriptive snapshot of the existing site — not the redesign target. Inferred sections marked.
---

# PRODUCT.md — Current State (Descriptive)

## Register

Brand. The site is a marketing/landing surface for the AEM Author Kit product, currently dressed
in Brazil World Cup editorial content as a demo theme. The underlying product is a developer
toolkit for AEM Edge Delivery Services.

<!-- _provenance: inferred — page reads as a product landing page with editorial demo overlay -->

## Users

Primary: AEM developers and content authors evaluating or onboarding to AEM Edge Delivery Services.
Secondary: AI agents (explicitly called out in the "Something for everyone" section — Authors /
Developers / Agents tabs).

<!-- _provenance: inferred from nav labels ("Get started", "Docs"), CTA targets (github.com/aemsites/author-kit, aem.live/developer/tutorial), and section copy ("Even AI agents can feel at home with Author Kit") -->

## Product Purpose

Author Kit is a starter template and component library for AEM Edge Delivery Services sites —
giving developers a fast path to a production-ready AEM site and giving authors a rich set of
blocks to compose pages without writing code.

Scope: single-page demo site showcasing the kit's blocks and capabilities with Brazil World Cup
editorial content as the live example.

## Brand Personality

Energetic, aspirational, and technically confident. The Brazil World Cup overlay gives the demo
a bold, editorial feel — but the underlying product voice is developer-friendly: direct,
capability-first, and slightly playful ("Even AI agents can feel at home").

<!-- _provenance: inferred from headline tone ("Brazil Goes for the Championship"), CTA copy ("Join the Journey", "Follow the Seleção"), and explicit agent-audience callout -->

## Anti-references

None explicitly captured from the live site.

## Design Principles

1. **Content-first blocks** — Every section is a self-contained, authorable block. The design
   system supports the content structure, not the other way around.
2. **Dark/light parity** — The site supports both light and dark modes natively via CSS
   `light-dark()` and explicit `dark-scheme` section overrides.
3. **Grid flexibility** — Sections use a flexible 12-column grid with utility classes
   (grid-2, grid-3, grid-4, bento) to compose diverse layouts from the same system.
4. **Performance-first** — AEM EDS architecture; images are optimized via the CDN pipeline.

## Accessibility & Inclusion

Language: `en`. Dark mode: supported. No RTL signals in the captured page.
