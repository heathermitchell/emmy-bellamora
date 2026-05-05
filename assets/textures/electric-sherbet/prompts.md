---
owner: emmy
date_created: 2026-05-05
status: living reference
type: texture-provenance
kit: electric-sherbet
---

# Electric Sherbet — Texture Generation Log

Provenance for kit textures. Every regen gets logged here: prompt, model, date, verdict.

---

## texture-tangerine-sorbet.png (currently live)

**Filename history:** previously `texture-tangerine-fizz.png` — renamed 2026-05-05 because (a) the file's actual content is sorbet, not fizz, and (b) renaming bypassed Cloudflare cache after the swap.

**Generation:** 2026-05-05
**Model:** kie.ai gpt-image-2 (text-to-image)
**Prompt:**
> Macro photograph of tangerine sorbet, no container, fills the frame completely, top-down, square composition.

**Why this prompt won:**
- "Sorbet" reads more vivid/saturated than "sherbet" (no dairy = sharper color)
- "No container, fills the frame completely" prevents the model from putting it in a bowl/glass — the brief was *the material itself*, not a vessel
- Simple wins. Earlier versions tried "liquid amber glass," "sun-warmed silk underneath," "bubbles rising through bright tangerine liquid" — model results got muddled. The shorter prompt produced cleaner output.

**Lesson — vocabulary betrays:** the original `texture-tangerine-fizz.png` (now retired) read as fish roe. "Fizz" + "tangerine" + macro photography pulls the model toward citrus pulp / caviar / fish roe. Use *material vocabulary* (sorbet, silk, velvet, glass) not *flavor vocabulary* (fizz, zap, shock).

**Status:** live as of 2026-05-05. Heather: "I think that's better. I'm still not 100% happy, but it's better than it was."

**Explorations folder:** `zcos/zc-peeps/emmy/brand-kits/sugar-on-top-cupcake-shop/electric-sherbet/textures/regen-explorations/` — has v1 (orange soda top-down), v2 (inside the soda side view), v3 (tangerine sherbet), v4 (tangerine sorbet, the winner).

---

## Other ES textures (provenance unknown)

The following textures exist in the kit but were generated before this log was started. Provenance is **unknown** — model, prompt, and date were not captured at generation time.

- `texture-fuchsia-shock.png`
- `texture-lemon-zap.png`
- `texture-lime-volt.png`
- `texture-midnight-mango.png`
- `texture-raspberry-velvet.png`
- `texture-sherbet-cream.png`
- `texture-twilight-grape.png`

If any of these get regenerated, log the new prompt here.

---

## Going forward

Every new texture generation in this kit logs here at the time of generation, not after. Same for all other kits — each kit gets its own `prompts.md` next to its texture files.
