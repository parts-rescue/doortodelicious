# Door to Delicious

Static rebuild of [doortodelicious.com](https://doortodelicious.com/) — the site of
Karen, an Independent Thermomix® Consultant in Door County, Wisconsin. Rebuilt
from the original WordPress.com site as plain static HTML/CSS for Cloudflare Pages.
No backend; the old `mailto:` link is replaced with a contact form.

## Two versions (comparison phase)

- **`/`** — recommended version: single page — sticky masthead, hero, what it does
  (+ photo strip), why a Consultant, About Karen, booking form, FAQ, footer.
  `index.html` + `styles.css`. Hand-written CSS, no framework.
- **`/original/`** — "original style": mirrors the live dark site as closely as
  possible, with only the Thermomix-required changes (see `docs/thermomix-compliance.md`).
  `original/index.html` + `styles-original.css`. `noindex`.

A `.preview-bar` at the top of each links to the other. Once Karen picks one,
delete the loser plus the preview bar.

## Design system (recommended version)

Everything is derived from Karen's own consultant seal, `assets/logo.png` — a
circular stamp with arced lettering, drawn in two inks on warm paper. All three
colours below are sampled straight out of that file:

| Token | Value | Role |
| --- | --- | --- |
| `--cherry` | `#a82334` | Action only — buttons, links |
| `--pine` | `#1d5a38` | Structure only — eyebrows, rules, checks, footer |
| `--paper-warm` | `#f9f8f4` | Alternating section bands (the seal's own paper) |

Two recurring devices carry the identity: the **seam** (two hairlines 3px apart at
the top of each band, echoing the seal's concentric rings) and **letterspaced caps**
in pine (the arced seal lettering, straightened). Type is Playfair Display for
display only — it matches the wordmark's high-contrast serif — with Inter for
everything else. Both are self-hosted variable woff2.

The seal itself is the hero image; the food photos are Karen's own phone shots, so
they run small and uniformly cropped rather than full-bleed.

## Structure

```
public/            <- everything that gets deployed (Worker assets directory)
  index.html       <- recommended version (light)
  styles.css
  original/
    index.html     <- original-style version (dark)
  styles-original.css
  404.html
  robots.txt
  sitemap.xml
  _headers         <- headers (security + caching)
  favicon.ico
  assets/          <- images (logo, food photos)
  fonts/           <- self-hosted woff2: Playfair + Inter (/), Haskoy + Rubik (/original/)
```

`assets/logo-mark.png` (376×379, 71 KB) is the web copy of the seal used on `/`;
`assets/logo.png` (752×758, 825 KB) is the full-resolution master, referenced only
from the JSON-LD.

## Local preview

```
cd public && python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy (Cloudflare Workers — static assets, Git integration)

Deployed as an assets-only Cloudflare Worker via Workers Builds. Config is
`wrangler.jsonc` (`assets.directory` = `./public`). The Git connection runs
`npx wrangler deploy` on every push to `main`.

- **Repo:** `parts-rescue/doortodelicious`, branch `main`
- **Build command:** none · **Deploy command:** `npx wrangler deploy` · **Root:** `/`

Test URL: enable `workers.dev` under the Worker's **Settings → Domains & Routes**
to get `https://doortodelicious.<subdomain>.workers.dev`. The custom domain
(`doortodelicious.com`) is only attached after the site is approved — nameservers
are not moved before then.

Local check: `npx wrangler dev` (serves `public/`), or just
`cd public && python3 -m http.server`.

## Contact form

Uses [Web3Forms](https://web3forms.com/) (no backend). The access key lives in the
hidden `access_key` field in `public/index.html`. The recipient address is
configured in the Web3Forms dashboard for that form — set it to an inbox Karen
checks and verify it there.

## Follow-ups

- The four food photos are 737×983 JPEGs (~150 KB each) but display around 260 px
  wide in the photo strip. Re-export them at ~600 px / as WebP when image tooling is
  available. They are lazy-loaded, so the initial page load is ~210 KB.
- `public/assets/logo.png` (825 KB) is kept as the master. The site loads
  `logo-mark.png` instead; re-export both as WebP when tooling allows.
- Karen's portrait (`public/assets/karen.jpg`, 960×958, 119 KB) is in place in the
  "About Karen" section. It is square and her face sits up and left of centre, so
  `.portrait img` scales to 118% and offsets to recentre her in the circle — redo
  that offset if the photo is ever swapped.
