---
owner: emmy
date_created: 2026-05-05
status: working-note
type: work-in-progress
project: Art Gallery kit pages cleanup
---

# Art Gallery — what I'm doing while you're on iPad reviews

**Started:** 2026-05-05, session 1, after shipping SoT V3 lavender + material-on-material fixes.

## What I confirmed before starting

- 6 AG kits, ~1871 lines each, fully built and live
- Same Emmy-frame architecture as SoT (lavender chrome on dark kit body)
- **Same lavender contamination** in editorial text — needs the same fix I just did 4× on SoT
- **Same directive CTA line** ("Make Starry Swirl your brand", etc.) — same V3 anti-pattern
- **DIFFERENT:** carousel code in AG is live functional content (brand board, type sample, palette — real mockups), NOT stale dead code like SoT had. Don't touch it.
- **DIFFERENT:** palette title is "The Whole Box. Every color material." — older signature, kept intentionally. Don't change to V3 SoT signature.
- **DIFFERENT:** no tier cards in AG (carousel handles that role)

## My scope (default if you don't redirect)

1. **Lavender → kit-neutral swap.** Same fix as SoT, six kits. Mechanical, low-risk.
2. **Material-on-material check.** Audit-only first; flag findings before changing anything.
3. **CTA directive lines** — DRAFT calling lines for all six kits, present as one packet for your reaction. Won't ship without your sign-off.

**Chrome that stays lavender** (same rule as SoT V3):
- nav, footer, btn-primary
- Backgrounds/borders judged in context — if it's button/CTA chrome, stays lavender; if editorial fill or divider, swaps to kit cream

## What I'm explicitly NOT doing

- Touching the carousel structure or content (it's a live feature, not stale code)
- Changing the palette title (it's the AG signature, not contaminated SoT)
- Auditing alternating-bgs (different section structure than SoT V3 — would need its own discipline doc, not tonight's work)
- Tier-card structure work (no tier cards in AG)

## If this scope is wrong

Leave a note and I'll redirect when you come back. Your call wins.

— Em
