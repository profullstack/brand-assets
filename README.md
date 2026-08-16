# Profullstack &amp; #Moshcoding brand assets

Logos, avatars, banners, badges, ad cards and video cuts for
[Profullstack, Inc.](https://profullstack.com) and [#Moshcoding](https://moshcoding.com).

**Live media kit:** <https://anthony.dev.profullstack.com/assets/>

This repository is a **mirror**. The live site is a plain directory served by nginx
(`~/public_html/assets/` on the dev box) — editing a file there *is* publishing. Nothing here
builds or deploys; this repo exists so the kit survives the box.

## What's in it

| Folder | Contents |
| --- | --- |
| `profullstack/` | Vector logo, square mark, app icon, X/profile header, 16:9 social card, background texture, two headshot avatars, 20-file favicon + touch-icon set, 16:9 and 9:16 brand spots |
| `moshcoding/` | 3 badges, 7 banners (four at 2048×682), 4 square covers, 4 ad cards, 2 icons, 14 video cuts |
| `paybadge/` | Two embeddable "accepts crypto" SVG shields |
| `previews/` | Compressed JPEGs used by the gallery page. **Not** for distribution — always ship the original |
| `index.html` | The media-kit page itself |

66 downloadable assets, ~213 MB.

## Where the originals come from

Everything was copied and renamed from three other repositories. Those remain the source of
truth — fix artwork there, then re-copy here:

- `profullstack/profullstack-web` → `public/assets/logo.svg`, `logo-white.png` (square mark),
  `logo-black.png` (the 2048×1152 social card), `channels_banner.jpg` (the `@ProfullstackInc`
  header), `assets/{bg.png,bg.svg,anthony.png,preshy.png}`, `icons/`, `profullstack-{16x9,9x16}.mp4`
- `moshcoder/moshcoding` → `images/moshcoding_*`, `videos/*.mp4`, `app/{icon,apple-icon}.png`
- `profullstack/paybadge` → `badge.svg`, `badge-large.svg`

## Gotchas

- In the moshcoding source, every `*_thumb.png` is a **same-size re-encode** of its non-thumb
  twin, not a smaller preview. `videos/finals/` duplicates two files in `videos/`.
  `paybadge/badge-crypto.svg` is byte-identical to `badge.svg`. All were deduped out.
- **`moshcoding/badges/moshcoding-badge-code-hard-302.png` has garbled lettering** — the arc text
  reads "CODE HARB RAS HARDEE". It ships with a warning on the page. Redraw it before any large
  or print use.
- Video cuts named `*-with-audio.mp4` carry a music bed that has **not** been cleared for paid
  distribution. Use the silent cuts for anything with money behind it.
- The `previews/` JPEGs were generated with Pillow (18 MB of art → 1.1 MB). The build box has no
  ffmpeg, ImageMagick or system PIL — use a throwaway `python3 -m venv` + `pip install Pillow` to
  regenerate. Video posters are brand stills, not extracted frames.

## Colors

Profullstack red `#E02337` (from the profullstack-web stylesheet), with `#0D0D0D` / `#1F1F1F` /
`#2A2A2A` neutrals and `#BA18AA` / `#6EE7A8` accents.

#Moshcoding greens `#A0B449`, `#7C9610`, `#4A5621` on `#000000` — these were **sampled from the
artwork**, not taken from a spec.

## Usage

Press and partners may use these as-is. Don't recolour the marks, stretch them, add effects, or
rebuild the wordmark in another typeface. Keep the Profullstack slash red.

Questions or a size that isn't here: anthony@profullstack.com
