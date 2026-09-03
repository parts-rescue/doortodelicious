# Door to Delicious

Static rebuild of [doortodelicious.com](https://doortodelicious.com/) — the site of
Karen, an Independent Thermomix® Consultant in Door County, Wisconsin. Rebuilt
from the original WordPress.com site as plain static HTML/CSS for Cloudflare Pages.
No backend; the old `mailto:` link is replaced with a contact form.

## Structure

```
public/            <- everything that gets deployed (Pages output directory)
  index.html       <- the single page
  404.html
  styles.css
  robots.txt
  sitemap.xml
  _headers         <- Cloudflare Pages headers (security + caching)
  favicon.ico
  assets/          <- images (logo, portrait, food photos)
  fonts/           <- self-hosted Haskoy (body) + Rubik (headings) woff2
```

## Local preview

```
cd public && python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy (Cloudflare Pages — Git integration)

Connect the GitHub repo `parts-rescue/doortodelicious` to a Cloudflare Pages
project:

- **Production branch:** `main`
- **Framework preset:** None
- **Build command:** *(leave empty)*
- **Build output directory:** `public`

Every push to `main` builds and deploys automatically. The test URL is
`https://<project>.pages.dev`. The custom domain (`doortodelicious.com`) is only
attached after the site is approved — nameservers are not moved before then.

## Contact form

Uses [Web3Forms](https://web3forms.com/) (no backend). Replace
`YOUR_WEB3FORMS_ACCESS_KEY` in `public/index.html` with the access key emailed to
`doortodelicious@gmail.com` after creating it at web3forms.com.

## Follow-ups

- `public/assets/logo.png` is ~800 KB — re-export smaller / as WebP when tooling
  is available.
