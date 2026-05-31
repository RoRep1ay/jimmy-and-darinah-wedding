# Wedding page — design arena synthesis

Explored 4 distinct font + vibe directions for the Evelyn & Julian page, then synthesized one.
Content (names, date, venue, captions) and behavior (countdown → `2026-09-21T16:00:00`,
scroll-reveal, reduced-motion) are identical across all of them.

## Candidates (kept as browsable files)
- `vibe-editorial.html` — Bodoni Moda + Jost · ivory/charcoal + oxblood · magazine masthead
- `vibe-romantic.html`  — Pinyon Script + EB Garamond · blush & champagne · gold ❧ fleurons
- `vibe-minimal.html`   — Fraunces + Space Grotesk · stone + terracotta · airy data-grid
- `vibe-deco.html`      — Cinzel + Jost · midnight-emerald + gold · sunburst & gem ornaments

## Cross-judge scores (independent reviewer)
C3 minimalist 30 · C4 deco 29 · C1 editorial 27 · C2 romantic 27. All preserved content
and behavior; spread was on responsive robustness and polish, not correctness.

## Base chosen: Romantic (C2)
The judge rated C3 the strongest *engineering* base, but the aesthetic is the couple's call —
they chose Romantic. So C2 is the base, and C3's robustness was grafted **in** to fix its gaps.
Final result is `index.html`.

## Grafts folded in
- **From minimalist (C3):** fluid `--gutter: clamp(20px,5vw,56px)` on wrap/hero/footer;
  a sub-440px breakpoint (gallery collapses to 1 column); and killing the looping
  `.scroll-cue::after` pulse under `prefers-reduced-motion` — C2's three real weak spots.
- **From art-deco (C4):** the gold inset "matted frame" on gallery photos
  (`.photo::before`, inset 6px, hover brightens), recolored to the champagne-gold palette.

## Rejected (and why)
- **Editorial masthead ribbon (C1):** too cold/editorial against a soft script hero — it would
  fight the romantic tone rather than support it.
- **Geometric gem deco-mark (C4):** C2's ❧ fleuron is the more romantic divider; a faceted
  gem motif reads as deco and clashes.

## Verified
All content strings present; countdown target, IntersectionObserver, and reduced-motion intact;
all grafts present; no undefined CSS variables; single self-contained file.
