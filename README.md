# River Crossing — Companion

An interactive HTML companion to TETC's "River Crossing" lesson — the classic
wolf-goat-cabbage puzzle adapted for the VEX AIM Coding Robot (90-minute Python
intro, 9th/10th grade). The HTML companion walks students from solving the
puzzle on paper, through Blocks, Switch, typed Python, and finally a loop
refactor that pays off the pain of Level 2.

Live site: https://tetc-edu.github.io/River-Crossing-Companion/

## What this bundle is

A single file, `index.html`, that is the complete, working artifact, plus
`field.html` as a separate field-reference page and `logo-tetc.png`. No build
step, no dependencies, no backend. Open it in any modern browser and it works.

Adapted from the
[Stadium Rover Companion](https://github.com/TETC-Edu/Stadium-Rover-Companion)
template — same layout, components, CSS tokens, and JS architecture; only the
lesson content differs.

## The lesson, at a glance

- **Cargo:** blue barrel = wolf, orange barrel = goat, sports ball = cabbage.
- **Field:** 100 × 100 cm. Students draw a river across the mat with an Expo
  marker (max 130 mm / 5 inches wide).
- **Rules:** never leave wolf+goat or goat+cabbage alone. The robot counts as
  a chaperone.
- **Goal:** get all three items across in **7 crossings**. Items can travel
  both directions.
- **Standard:** CSTA 1B-AP-11 (Decomposition).

## The arc

1. **Overview** — hook, the rule, safe/unsafe combos, sample setup, path picker.
2. **Level 1 — Blocks.** Solve on paper first, then code it.
3. **Level 2 — Switch.** Redraw the river. Convert blocks to read the Python.
   Fix every number for 7 trips.
4. **Level 3 — Python.** New river. Type all 7 crossings from scratch.
5. **Bonus — Loops & variables.** Refactor into one `for` loop over a list of
   7 trip tuples with `"place"` / `"none"` actions.

## State / persistence

`localStorage` key: `tetc_river_crossing_companion_v1`. Shallow-merged on load
so new keys don't wipe saved state. Tracks path, current screen, completions,
failure-log text, and per-hint reveal counts.

## Hosting

GitHub Pages on `main`. URL: `https://tetc-edu.github.io/River-Crossing-Companion/`.
