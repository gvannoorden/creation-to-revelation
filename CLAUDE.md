# CLAUDE.md — creation-to-revelation

Interactive Gantt-style Bible timeline, creation to about AD 100. Personal project.
Live at https://gvannoorden.github.io/creation-to-revelation/ (GitHub Pages, `main` branch root, no workflow).
Listed on the splash page `gvannoorden.github.io` as a card in The Works.

## Constraints

- **One file.** Everything is in `index.html`: CSS, JS, and all data. No build step. `.nojekyll` skips the Jekyll pass.
- Only external request: Google Fonts (Barlow Condensed, Source Serif 4), with fallbacks.
- Browser storage keys: `ctr-lanes` (lane order and visibility), `ctr-theme` (light/dark). Wrap any new storage in try/catch.
- Theming: colors are tokens on `:root`; dark values are written twice on purpose, once under `prefers-color-scheme: dark` scoped to `:root:not([data-theme="light"])` and once under `:root[data-theme="dark"]`. Keep them in sync.

## Data model (in the `/* ---------- Data ---------- */` block)

- Years are numbers: **BC positive, AD negative** (AD 30 = -30). There is no year 0.
- Undated items before Abraham use `start: PRE` and a `pre: [fromFraction, toFraction]` placement inside the not-to-scale zone (`PRE_W` px wide).
- `views` is a string of the levels an item shows in: `o` overview, `s` standard, `d` detailed.
- `group` decides the lane (see `GROUPS`). `coStart` draws a hatched coregency or rival reign in Detailed view; `window: true` draws a dashed dating window; `alt: [start, end, label]` draws a dotted alternate-date bar when "Show alternate dates" is on.
- Books of the Bible are parsed from each item's `refs` string via `ABBR`; keep refs in the abbreviated form already used (e.g., `1 Kgs 12:1–24`).

## Dating sources

Kings: Thiele, as refined by Young (JETS 2005). Patriarchs to judges: exodus 1446 from 1 Kgs 6:1, 430 years in Egypt (Exod 12:40), Merrill. The in-app About panel is the user-facing explanation; update it when a dating choice changes.

## Preview

`python3 -m http.server 4713`, then http://localhost:4713.
