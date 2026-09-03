# Door to Delicious

This is a from-scratch rebuild of a WordPress site as a static site for Cloudflare Pages. The site is Doortodelicious.com. The business is a Thermomix consultant page. No backend is needed. A contact form should replace the current mailto link.

## Deployable site

Everything that ships lives in `public/` (Cloudflare Pages output directory). Plain
static HTML/CSS, no build step. Preview locally with `cd public && python3 -m http.server`.

## Thermomix compliance — required

`docs/thermomix-compliance.md` lists Thermomix/Vorwerk rules that **must** be
followed on this site. Read it before editing anything in `public/` and keep the
build compliant: independent-consultant identity near the top and in the footer,
the footer legal disclaimer on every page, `Thermomix®` with the ® symbol, no
on-site cart/checkout/pricing, and no specific incentive dollar amounts unless
Thermomix's official materials use that figure.
