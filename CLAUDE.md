# Door to Delicious

This is a from-scratch rebuild of a WordPress site as a static site for Cloudflare Pages. The site is Doortodelicious.com. The business is a Thermomix consultant page. No backend is needed. A contact form should replace the current mailto link.

## Deployable site

Everything that ships lives in `public/` (Cloudflare Pages output directory). Plain
static HTML/CSS, no build step. Preview locally with `cd public && python3 -m http.server`.

## Thermomix compliance — required

`docs/thermomix-compliance.md` lists Thermomix/Vorwerk rules that **must** be
followed on this site (trademark/identity rules + the Social Media & AI Cheat
Sheet). Read it before editing anything in `public/` and keep the build
compliant. Key points:

- Independent-consultant identity near the top and in the footer; footer legal
  disclaimer on every page; `Thermomix®` with the ® symbol.
- No on-site cart/checkout/pricing; orders go to `shop.thermomix.com/consultant/109102`.
- **No personalized incentives** ("$X gift card when you order through me", "free
  gift from me"); describe only the standard/national offer, no dollar figures
  unless official materials use them.
- **No income / earnings / lifestyle claims**; no consultant-recruitment content.
- **Only approved/authorized brand images** — prefer Karen's own photos.
- **AI-assisted copy must be reviewed and approved by Karen** before it ships;
  **no AI auto-reply, chatbot, or AI-written testimonials/reviews** on the site.
