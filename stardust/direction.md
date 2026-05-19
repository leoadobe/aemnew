# stardust/direction.md

---

## # Active Direction — 2026-05-18

### Phrase (verbatim)

> "i have a challenge, this year we will have the world cup and i would like to change my design
> to reflect the world cup, especialli the brazilian national team, the most winner of the
> championship. i would like to emphasize brazilian colors and vibe to transmit the idea of world
> cup to the brazilian audience"

### Restatement (dimensional)

Redesign the visual surface of the Author Kit demo site to embody a Brazil World Cup campaign.
Replace the current purple/magenta palette with Brazilian national colors (verde, amarelo, azul).
Amplify type weight and scale to match the energy of a sports campaign. Orient tone toward a
Brazilian audience celebrating the Seleção's pursuit of a sixth World Cup title. Keep the
existing 11-section page structure intact (verbatim IA fidelity).

### Movements

| Axis | From | To | Source |
|---|---|---|---|
| palette | purple `#9d60d8` / magenta `#bd0084` | verde `#009C3B` / amarelo `#FFDF00` / azul `#002776` | user-explicit |
| expressive | restrained (wght 600 display) | committed (wght 900 display / 800 headings) | user-phrase + register |
| type scale ratio | 1.122 | 1.25 | committed expressive tier |
| tone | neutral / product | passionate, celebratory, national pride | user-phrase |
| audience | developer-generic | Brazilian football audience | user-explicit |
| register | brand | sports campaign | resolved from phrase |
| density | packed (48px) | **balanced (64px)** | user-answer Q1 |
| ia-fidelity | — | **verbatim** | user-answer Q2 |

### Questions & Answers

**Q1 — Density:** Balanced (64px section padding, energetic but breathing room between sections).
Hard floor honored: 11 sections → ≤ 64px cap; balanced lands exactly at the cap.

**Q2 — IA fidelity:** Verbatim. Same 11-section structure, surface transformation only.
Section sequence, presence, and IA priorities are locked.

### Mode Detection

**Mode: Targeted palette rebrand.** Brand signal was `signal-strong` (Montserrat + 5-color
palette), which would normally activate Mode A (brand-faithful). However, the user's phrase
explicitly requests "emphasize Brazilian colors" — a direct palette change signal that overrides
Mode A's palette pin. Type (Montserrat) is PINNED as brand-inherited; palette is REPLACED.

Mode A constraint released for: palette only.
Mode A constraint retained for: type family, type scale (now lifted to 1.25 as part of expressive
movement, not a rebrand — Montserrat at 1.25 ratio is still Montserrat).

### Divergence Seed

| Dimension | Value | Picked by |
|---|---|---|
| Decade | 2025-now | context — current World Cup year |
| Craft | sports-campaign / CBF-kit-tradition | anchor: Brazilian football visual culture |
| Register | Campaign | resolved from phrase |
| Ground-family | stark-white | brand-faithful override — existing white ground preserved; azul is alt-section surface |
| Font deck | brand-inherited (Montserrat) | type pin |
| Palette | Brazilian national colors | user-explicit |

### Resolved Direction Summary

**Verde** `oklch(57% 0.165 145)` → brand, borders, decorative, large-text surfaces.
**Amarelo** `oklch(91% 0.185 95)` → CTAs (always with azul text, 13:1 AAA), highlights.
**Azul** `oklch(22% 0.095 265)` → dark sections, deep text, CTA text on amarelo.

Montserrat at wght 900 display, 800 headings. Scale ratio 1.25. Section padding 64px desktop.

### Anti-toolbox Audit

- National-flag palette: NOT a reflex pick — user-explicit, brand-specific. ✓ PASS
- Hero text on photography: HIT — mitigated by verde/azul gradient scrim requirement in DESIGN.md.
- Generic SaaS silhouette: GUARDED by anti-references in PRODUCT.md.
- Gradient text: FORBIDDEN — recorded in DESIGN.md donts.
- Glassmorphism: FORBIDDEN — recorded in DESIGN.md donts.

### Command Sequence (for prototype)

```
$impeccable craft  — render home-proposed.html with Brazilian palette + heavy type
$impeccable colorize  — if verde/amarelo balance needs tuning
$impeccable bolder  — if type weight needs further amplification
$impeccable adapt  — mobile responsiveness at 375/414/640/768/1024/1280/1440/1920
$impeccable polish  — final refinements
```

### State

- Direction resolved: 2026-05-18T23:30:00Z
- Pages directed: 1 (home)
- Stale prototypes: 0 (none exist yet)

### Confirmed by user

User typed "go" — direction confirmed 2026-05-18.

---

*Re-directs append below this line as new sections.*
