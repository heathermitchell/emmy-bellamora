---
owner: emmy
date_created: 2026-05-03
status: living-reference
type: workflow-note
---

# How emmybellamora.com gets built and shipped

**This is the only site folder.** If you find another one, it's stale — check `zcos/zc-peeps/emmy/_archive/`.

## The setup

- **Local working dir:** `~/Documents/emmy-biz/_emmy-bellamora/` (this folder — the vault-side path listed here originally no longer exists)
- **Git repo:** has its own `.git` — separate from the vault's git repo
- **Remote:** `https://github.com/heathermitchell/emmy-bellamora.git`
- **Live site:** `https://emmybellamora.com` (Cloudflare Pages, auto-deploys on push to `main`)

## The publish flow

```bash
cd zcos/zc-peeps/emmy/emmy-bellamora
# make changes
git add <files>
git commit -m "..."
git push
# Cloudflare auto-deploys, usually live within ~1 min
```

That's it. No build step. Static HTML/CSS/assets, deployed as-is.

## Why two pushes matter

This folder lives **inside** the vault, but it's a **separate git repo**. So the vault commits and pushes do nothing for the live site. Pushing the vault doesn't ship anything to emmybellamora.com.

Heather made the call (2026-05-03) to keep it inside the vault rather than move it back to `~/Documents/`. Reason: vault keeps everything Emmy in one place, and the extra `cd && git push` is small friction.

## Where to find things

- **Home page:** `index.html`
- **Kit pages:** `kits/sugar-on-top/[kit].html`, `kits/art-gallery/[kit].html`
- **Textures (PNG):** `assets/textures/[kit-name]/[material].png`
- **Workers config:** `wrangler.toml` (Cloudflare)

## Source material for kit pages

The HTML pages here are the OUTPUT. The brand kit source material (palettes, typography selections, brand boards, playgrounds) lives at:

- `zcos/zc-peeps/emmy/brand-kits/sugar-on-top-cupcake-shop/[kit-name]/`
- `zcos/zc-peeps/emmy/brand-kits/art-gallery/[kit-name]/`

If you're rebuilding a kit page, pull palette + typography + scene story from those folders. That's where Heather and I built the kits originally.

## Cloud Pages quirks to know

- Clean URLs: `https://emmybellamora.com/kits/art-gallery/starry-swirl` (no `.html` suffix). Cloudflare strips it.
- `file://` previews: `_build/work-screenshots/` is for local mockups. Don't link to anything in `_build/` from the live site.

## When in doubt

Run `git remote -v` from this folder. If you see `emmy-bellamora.git`, you're in the right place. If you see anything else (or no remote), you're in the wrong folder.

— Emmy
