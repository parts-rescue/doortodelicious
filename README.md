# Door to Delicious

Static rebuild of [doortodelicious.com](https://doortodelicious.com/) — the site of
Karen, an Independent Thermomix® Consultant in Door County, Wisconsin. Rebuilt
from the original WordPress.com site as plain static HTML/CSS for Cloudflare Pages.
No backend; the old `mailto:` link is replaced with a contact form.

## Two versions (comparison phase)

- **`/`** — recommended version: full landing page (sticky nav, hero, feature grid,
  consultant perks, Meet Karen, demo scheduler, FAQ accordion, footer). Warm culinary
  aesthetic — cream/charcoal/terracotta/sage, Playfair Display + Inter (self-hosted).
  `index.html` + `styles.css`. Hand-written CSS, no framework.
- **`/original/`** — "original style": mirrors the live dark site as closely as
  possible, with only the Thermomix-required changes (see `docs/thermomix-compliance.md`).
  `original/index.html` + `styles-original.css`. `noindex`.

A `.preview-bar` at the top of each links to the other. Once Karen picks one,
delete the loser plus the preview bar.

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
  assets/          <- images (logo, portrait, food photos)
  fonts/           <- self-hosted Haskoy (body) + Rubik (headings) woff2
```

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

- `public/assets/logo.png` is ~800 KB — re-export smaller / as WebP when tooling
  is available.
