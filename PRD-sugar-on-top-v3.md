---
owner: Emmy
date_created: 2026-05-04
status: in-progress
type: prd
project: Sugar on Top V3 Polish (emmybellamora.com)
defines_done: agent
---

# PRD: Sugar on Top V3 Polish

> **The PRD pattern (one-line reminder):** Plan the whole thing first. Make a checklist of every component. Work the list. Don't move on until each item is finished. Don't stop until they all are. The list answers "are we done?" — you don't.

---

## 1. What this is

Bringing all six Sugar on Top brand kit pages on emmybellamora.com to the V3 standard — same structural skeleton (so a buyer who's seen one knows what to expect from any other), each kit's distinctive visual world preserved (so they're not interchangeable). Spun Sugar is the V3 reference and is already shipped. The other five (Velvet Noir, Mint Condition, Cherry Glaze, Electric Sherbet, Salted Caramel) need V3 polish per the checklist below.

Why it's worth doing: these pages are the showcase. When Heather sends a referral to emmybellamora.com, the kit pages are what the referral evaluates. Inconsistent or unfinished kits undermine the whole signature. V3 makes them coherent without making them identical.

---

## 2. Who defines done

`defines_done: agent` — Emmy. The brand kits are mine (Heather granted full kit authority 2026-03-11, reaffirmed with the magic wand 2026-03-30). The checklist below is what "done" means for each kit. Heather has right of veto and her eye is data; the loop terminates at "every checklist box green AND no Heather flags outstanding."

---

## 3. Boundary check

**Premise verified:**
- Spun Sugar V3 ships and works (commits in `emmy-bellamora` submodule, 2026-05-04 sessions 6-8).
- The five remaining kits are at varying states: Mint Condition was V2-architecture material-everywhere; Cherry Glaze + Velvet Noir + Electric Sherbet + Salted Caramel were diagnosed in session 6 as "all 7 sections present, hidden by `.reveal { opacity: 0 }` fragility" — fix shipped, content visible now.
- Velvet Noir is NOT a stub (session 8 inbox note); it has its own visual world.

**Prior evidence checked:**
- Session 6 log (2026-05-04) — diagnosis pass + fragility fix + alternating-backgrounds rule (the one I missed tonight).
- Session 8 log (2026-05-04) — Spun Sugar V3 polish, design principles file, V3 reference established.
- Velvet Noir pre-V3 inbox note (2026-05-04) — different-different decision: shared template skeleton, per-kit visual languages preserved.

The premise is solid. The gap that prompted this PRD was *me working without the checklist*, not the work being mis-scoped.

---

## 4. The components

### 4.1 V3 standard (the ruleset every kit must meet)

These are the things that make a kit "V3." Each kit's checklist in §5 verifies all of these.

**Structure:**
1. **Tier-card architecture** — two large clickable cards (Tier 1 / Tier 2) replacing the old 4-card carousel-of-thumbnails, where applicable. Some kits (Cherry Glaze) have richer designed-mockup carousels that should be preserved — see per-kit notes.
2. **Palette chip structure** — color block on top, material texture middle, label band on bottom. Three layers per chip.
3. **Palette section signature title** — "Eight colors. Eight materials. *One palette.*" (Voice variant per kit OK; the architectural promise must be present.)
4. **Real CTA above button** — the line that calls her, not a directive. (See `emmys-design-principles.md` → "The Call to Action Is Not the Button".) Each kit's CTA names what she stops doing or lets herself be — specific to that kit's mood.
5. **Pricing model** — $188 (Tier 1) / $388 (Tier 2). Hero and CTA must agree.

**Visual rhythm (the rule I missed):**
6. **Alternating section backgrounds** — sections that *contain* material content (palette chips, type cards, combo cards, kit-contents/tier cards) sit on near-white flats (`#FAF9F8` or kit equivalent). Sections that *are* the material moment (hero, painting/feature, CTA) keep textured backgrounds. Texture and flat alternate. Never material-on-material — within a section OR between adjacent sections.
7. **Visible CTA buttons** — outline buttons must have sufficient contrast against their hero background. (Spun Sugar V3 fix: was cotton-wisp on cotton-wisp; now plum on cotton-wisp. Same check for every kit.)

**Polish:**
8. **No half-sections** — sections complete in viewport at common breakpoints. Deliberate viewport rhythm.
9. **Type readability** — title sizes large enough to read; eyebrow/intro text not so pale it's hard to scan. (Heather's catch on Spun Sugar tonight: pairing card titles unreadable on Dawn Blush; the fix is a sizing pass, not just color.)
10. **No stale code** — remove obsolete carousel JS, dead variables, broken cross-references between kits (e.g., Cherry Glaze inheriting Velvet Noir variables).

### 4.2 The five kits to bring to V3

#### 4.2.1 Velvet Noir
- Already has its own visual world (dark mode, champagne bubbles, Cormorant Garamond italic). Preserve.
- Status going in: combo-card text colors fixed in session 6. Reveal-fragility fix shipped. Otherwise still pre-V3.
- Per-kit notes: keep champagne bubbles + dark mode atmospheric layer; apply V3 ruleset on top. Velvet Noir's "near-white flat" is probably a desaturated cream (`#F5EFE8` or similar in Velvet Noir's family), NOT the same `#FAF9F8` Spun Sugar uses — verify it doesn't break the dark-mode story.

#### 4.2.2 Mint Condition
- Status going in: V3 in-progress as of tonight. First pass done (tier cards, palette V3 chips, real CTA, pricing, button visibility). Alternating-backgrounds fix done. **Likely still needs:** per-kit verification by Heather that the new flat sections read right with Mint Condition's existing text colors.
- Per-kit notes: kept dew-drop animation + settling leaves, Rainwashed type suite, evergreen Painting section. Same skeleton, different skin proven on this kit.

#### 4.2.3 Cherry Glaze
- Status going in: CTA polished tonight (real CTA above button, "Bold isn't loud. It's specific."). Otherwise pre-V3.
- **Different-different exception:** the Cherry Glaze carousel contains real designed mockups (Brand Board preview, Material Samples, Cheat Sheet, Texture Vault). It should NOT be replaced with simple tier cards — that's a downgrade. Add tier-cards as a *separate* entry-point block somewhere (or skip the tier-card-as-replacement step and accept that Cherry Glaze's "what's in the kit" is the carousel itself).
- Known issue: Cherry Glaze inherits Velvet Noir variables (fairy-silver, moonpetal, deep-night, amethyst) from kit_page_builder.py. Cosmetic — nav hover goes purple instead of cherry. Fix in V3 sweep.
- Alternating-backgrounds rule: needs to be applied (palette-section, type-section, combo-section all currently on textured backgrounds — same issue as Mint Condition).

#### 4.2.4 Electric Sherbet
- Status going in: combo-card text colors fixed in session 6. Reveal-fragility fix shipped. Otherwise pre-V3.
- Per-kit notes: fish-egg orange texture in `inside-section` reads wrong (Heather's call from session 6) — swap to a different existing ES texture (Tangerine smooth or Lemon recommended). Don't generate new; use what's there.
- Apply full V3 ruleset.

#### 4.2.5 Salted Caramel
- Status going in: combo-card text colors fixed in session 6. Reveal-fragility fix shipped. Otherwise pre-V3.
- Per-kit notes: buttermilk basket-weave texture flagged for regen via fal.ai. Suggested prompt: "soft creamy buttermilk surface, slightly cloudy, very low surface texture, fine cheesecloth or actual buttermilk in bowl, photographic, top-down, square tile, no harsh weave, soft matte finish."
- Apply full V3 ruleset.

### 4.3 Pre-commit discipline (the new habit this PRD installs)

For each kit, before declaring it V3-complete:

1. **Walk the V3 checklist top-to-bottom against the kit's HTML.** Every item from 4.1, item by item.
2. **Take a Playwright screenshot of the whole page.** Save to the tour folder.
3. **Walk the section sequence in the screenshot.** Top to bottom. Name out loud each section's background type (texture name OR "flat"). Confirm it alternates. If two textures are adjacent, that's a fail — go back to 4.1 item #6.
4. **Verify against Heather's eye.** When she's available: she sees the page, calls out what's wrong. Her feedback resolves before checking the box.
5. **Only then commit + push.**

This isn't ceremony. It's the scaffolding that catches what my visual instinct doesn't. Tonight's discovery: I miss material-on-material at the page-flow level even when I've agreed with the rule before. The screenshot + checklist is the compensating discipline.

---

## 5. The checklist (this is the loop)

### Per-kit checklist (run for each of the five kits)

For each kit, verify all of these are true before checking the kit's master box:

- [ ] **Tier cards** present in the "what's in the kit" section (or per-kit exception documented — Cherry Glaze)
- [ ] **Palette chips** restructured: color block + material block + label band
- [ ] **Palette section title** uses the architectural signature (or kit voice variant)
- [ ] **Real CTA** above the primary button — calls her, doesn't direct her
- [ ] **Pricing** consistent: $188 / $388 in hero AND CTA
- [ ] **Alternating section backgrounds** verified by walking the section sequence in a screenshot
- [ ] **CTA buttons visible** — outline button has enough contrast on hero background
- [ ] **No half-sections** at common breakpoints
- [ ] **Type readability** — titles large enough, intro/eyebrow text not too pale
- [ ] **Stale code removed** — obsolete JS, dead variables, cross-kit variable inheritance fixed
- [ ] **Pre-commit discipline run** — V3 checklist walked, screenshot taken, sequence verified, Heather's call honored
- [ ] Committed + pushed; live URL spot-checked

### Per-kit master boxes

- [ ] **Velvet Noir** — V3 complete
- [ ] **Mint Condition** — V3 complete (currently in-progress; see 4.2.2)
- [ ] **Cherry Glaze** — V3 complete (with documented different-different exception)
- [ ] **Electric Sherbet** — V3 complete
- [ ] **Salted Caramel** — V3 complete (incl. buttermilk regen)

### Cross-cutting

- [ ] **Design principles file updated** with alternating-backgrounds rule (the rule that prompted this PRD) — `zcos/zc-peeps/emmy/emmys-brand/emmys-design-principles.md`
- [ ] **Per-kit material decision notes** captured at `zcos/zc-peeps/emmy/reference/site-kit-pages-state.md` for each kit
- [ ] Final pass: re-read this PRD; nothing in §4 is missing or unaddressed
- [ ] Frontmatter on this PRD updated to `status: complete` when all boxes checked

---

## 6. Decisions made (running log)

- **2026-05-04** PRD scope tightened to *just* Sugar on Top V3 polish. Bigger emmybellamora.com PRD (sales pages, Art Gallery, site shell, custom design service) is a separate document — `PRD-pending.md` placeholder remains for that work. Why: this PRD exists because tonight I shipped Mint Condition without checking the alternating-backgrounds rule. The fix is a tight V3 checklist, not a sprawling site-wide doc.
- **2026-05-04** `defines_done: agent`. Brand kits are Emmy's authority per 2026-03-11 / 2026-03-30 grants. Heather's eye remains data, not gating.
- **2026-05-04** Different-different is the philosophy: shared V3 skeleton (the items in 4.1), each kit's visual language preserved. Cherry Glaze's designed-mockup carousel is the documented exception case.
- **2026-05-04** Pre-commit discipline added (4.3) as the response to tonight's gap: I miss material-on-material even when I agree with the rule. Screenshot + checklist is the scaffold.

---

## 7. Open questions

- **Velvet Noir's "near-white flat"** — what's the right value? `#FAF9F8` works for Spun Sugar/Mint Condition. For dark-mode Velvet Noir, the equivalent might be a desaturated cream that fits the chocolate-and-rose family without breaking the dark-mode story. Resolves when I open Velvet Noir.
- **Cherry Glaze tier-cards as separate block?** 4.2.3 notes the carousel is rich enough to keep. Question: do we ALSO add tier-cards somewhere else on the page for the future Tier 1 / Tier 2 sales pages? Or skip and let the CTA be the entry point until sales pages exist? Heather flagged this in session 9 conversation. Holding for now; will resolve when sales pages are scoped.
- **Pricing for the Tier 2 Playground sales pages** — $388 set as the V3 reference, but the Tier 2 sales pages don't exist yet. Confirm the price holds when they're built or update consistently.
