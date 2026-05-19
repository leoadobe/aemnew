<!--
_provenance:
  writtenBy: stardust:direct
  writtenAt: 2026-05-18T23:30:00Z
  readArtifacts:
    - stardust/current/_brand-extraction.json
    - stardust/current/brand-review.html
    - stardust/current/pages/home.json
  stardustVersion: 0.7.1
-->

# Improvements — home

1. **[brand-coherence]** The current visual system uses purple `#9d60d8` and magenta `#bd0084` — colors with zero connection to Brazil, the World Cup, or the Seleção. A visitor landing on a page full of football photography and "Jogo Bonito" copy encounters purple buttons and a magenta accent. The mismatch destroys the campaign illusion.
   *Fix:* Replace entire color system with Brazilian national colors — verde `#009C3B`, amarelo `#FFDF00`, azul `#002776`. CTAs become amarelo-on-azul (13:1 contrast, unmistakably Brazilian).

2. **[expressive-underuse]** Montserrat is a variable font supporting wght 100–900, but every heading on the page renders at wght 600. For a World Cup campaign targeting Brazilian fans, 600 reads as "developer docs" not "Maracanã". The font can roar at 900 — it is not being asked to.
   *Fix:* Hero H1 at wght 900, section H2s at wght 800, eyebrow labels at wght 700 uppercase. Type scale ratio lifted from 1.122 → 1.25 (committed tier) so the headline hierarchy reads at arm's length.

3. **[lcp + a11y]** Two surfaced tensions from brand-review: (a) `T-lcp-no-eager` — the first rendered `<img>` has `about:error` as src; the actual first football photo (`media_1300083…`) is lazy-loaded, delaying LCP. (b) `T-h1-level-regression` — a header H2 ("Default header promo") precedes the page H1 in DOM order, violating heading hierarchy for screen readers and crawlers.
   *Fix:* Hero image gets `loading="eager"` + `fetchpriority="high"`. Header H2 demoted to `<p aria-label>` or removed.

4. **[missed-opportunity]** Eight football photographs (action shots, team celebrations, 1600px+ wide) render as modest card thumbnails inside the features grid. The Seleção's photography is the strongest emotional asset on the page — the layout buries it.
   *Fix:* Feature cards render images at minimum 480px wide, 16:9 aspect ratio. The hero image is explicitly full-bleed with a left-anchored headline overlay and a verde/azul gradient scrim for text contrast.

5. **[cta-incoherence]** Primary CTA "Join the Journey" links to `github.com/aemsites/author-kit` — coherent for the developer audience, wrong for a Brazilian football audience who has no idea what that GitHub repo is. The secondary CTA "Follow the Seleção" links to `aem.live` — equally confusing for a non-developer.
   *Fix:* Render both CTAs with `[data-placeholder]` visual signature and flag in `_provenance.unsourcedContent[]` so migrate can replace with audience-appropriate targets. Copy is preserved verbatim from capture; only the visual treatment signals the placeholder status to reviewers.
