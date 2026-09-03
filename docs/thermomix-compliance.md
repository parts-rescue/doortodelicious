# Thermomix® / Vorwerk consultant compliance

Thermomix company rules that **must be followed** for an Independent Consultant
website. Any change to `public/` must keep the site compliant with everything
below. Two source documents:

1. Trademark / independent-identity rules (table in §1).
2. The Thermomix **Social Media & AI Cheat Sheet** (§2) — "I Can" / "I Cannot"
   rules issued to consultants. Several apply directly to this website and to the
   fact that it was drafted with AI assistance.

When in doubt, Karen asks her Branch Manager or emails the Thermomix Marketing
Team (Marketing@Thermomix.us) **before** it goes live.

---

## §1 — Website identity & trademark rules

| Element | Rule | Status in this build |
| --- | --- | --- |
| **Domain name** (`doortodelicious.com`) | Keep as-is. Personal branding, no trademark in the name. | ✅ Compliant. |
| **No trademark in name/handle** (Cheat Sheet "Cannot" #7 — no "thermomix", "thermo" or similar in account name, username, handle) | — | ✅ Compliant — domain and site title are "doortodelicious". |
| **Independent identity** | "Independent Thermomix® Consultant" prominent near the top **and** in the footer. | ✅ Compliant — tagline under the header, footer line, `<title>`, meta description, About section. |
| **Legal disclaimer** | Standard footer disclaimer distinguishing the site from Vorwerk LLC. | ✅ Compliant — footer `.disclaimer`: independent, not operated/endorsed/sponsored by Vorwerk LLC, does not represent Vorwerk's position, trademark credited to Vorwerk International & Co. KmG, orders/payments handled directly by Vorwerk LLC. |
| **Cart / booking system** | Direct visitors to "Schedule a Demo" / personal consultation; no on-site cart. | ✅ Compliant — no cart/checkout/pricing; "Schedule a Demo" opens the contact form; orders go to `shop.thermomix.com/consultant/109102`. |
| **Trademark symbol** | Write **Thermomix®** with the ® on prominent uses, incl. "Thermomix® TM7". | ✅ Compliant. |

---

## §2 — Social Media & AI Cheat Sheet (as issued to consultants)

### ✅ I Can
1. **Identify myself by role** (e.g., Consultant, Team Leader) on social media.
2. **Act with integrity and kindness** in every post, comment, and message.
3. **Share my story** — daily life, passions, and tips that make my page feel personal.
4. **Be visible** by focusing on my business — recipes, tips, and real results.
5. **Attract and build loyalty** with new and existing customers organically.
6. **Post national offers** as soon as they're released, using **only approved visuals**.
7. **Use AI as a starting point** — for brainstorming captions or ideas — as long as I
   personalize, fact-check, and approve everything before it goes out under my name.
8. **Share, comment, like and repost** content from the @ThermomixUSA channel.

### ❌ I Cannot
1. **Engage in conduct that could damage the brand** (e.g., aggressive sales or recruitment tactics).
2. **Post classified ads** on Facebook Marketplace, eBay, OfferUp, Craigslist or similar buy-and-sell sites.
3. **Post paid advertising** of any kind without brand approval.
4. **Use brand logos, images or footage** without the appropriate authorization.
5. **Offer personalized incentives** on top of the current offer (e.g., a gift to attract a Customer).
6. **Make income or lifestyle claims** or suggest guaranteed earnings (e.g., "financial freedom").
7. **Use the company's trademarks** or similar in account name, username, or handle (e.g., thermomix, thermo).
8. **Publish AI-generated content as-is** — no unreviewed AI copy, images, video, or voice
   representing the brand, and no AI "reviews" or testimonials.
9. **Use AI tools to impersonate a real person**, fabricate results/testimonials, or auto-reply to
   prospects pretending to be human-written when it isn't disclosed.
10. **Create my own assets to support national offers** (e.g., additional assets to showcase
    0% APR Financing or an Exclusive Bundle).

### A note on AI
AI can help draft ideas faster, but it cannot replace Karen's voice, judgment, or brand
approval. Never let an AI tool post, message, or represent the brand on her behalf without
a human reviewing it first. Treat AI-generated content the same as any unapproved ad —
if in doubt, don't post it.

---

## §3 — How §2 applies to this website

| Cheat Sheet rule | Application to the site | Status / action |
| --- | --- | --- |
| **Cannot #4 — brand images without authorization** | The hero "portrait" image (`public/assets/thermomix.jpg`) is a **Thermomix marketing creative** ("It actually cooks for you", product shot, thermomix logo), carried over from the old site. | ⚠️ **Action for Karen:** confirm this is an approved consultant/national-offer visual. If it is not on the approved-assets list, replace it with one of Karen's own photos. Same check for `assets/logo.png` (Karen's own consultant logo — should be fine, but confirm it was provided/approved). |
| **Cannot #5 — personalized incentives to attract a Customer** | Old site said "**A $50 gift card exclusively when you order through my consultant link**" — a personalized incentive. A later redesign brief (from Gemini) asked to re-add a "$50 Exclusive Gift Card … through Karen's consultant link" badge + "Order with Exclusive Perks" CTA. **Not implemented.** | ⚠️ The recommended page (`/`) describes only "the current factory promotion" and "the official accessory voucher awarded when you choose a Consultant" — no dollar figure, no "exclusive through my link", CTA is "See Current Offers". **Action for Karen:** confirm with her Branch Manager that the voucher and "white-glove welcome & setup" wording describe the standard offer / normal consultant service. |
| **Cannot #6 — income / lifestyle / earnings claims** | The site sells consultation services to buyers; it does **not** recruit consultants and makes no earnings claims. | ✅ Compliant. Keep it that way — no "join my team" / "financial freedom" / earnings content. |
| **Cannot #3 & #10 — paid ads / self-made national-offer assets** | The site is an organic personal-branding page, not paid advertising. No homemade graphics promoting financing or bundle offers. | ✅ Compliant. Do not add DIY banners for 0% APR, "Exclusive Bundle", price promos, etc. National-offer promotion uses approved visuals only. |
| **Cannot #8 — publishing AI content as-is** | This site's structure and some copy (contact-form intro, meta descriptions, alt text, footer disclaimer wording) were drafted with AI assistance. Karen's own words from the old site were preserved. | ⚠️ **Action for Karen:** read every line of `public/index.html` and approve it as her own voice **before** the domain is pointed here. This is the human review the rule requires. |
| **Cannot #9 — AI impersonation / auto-reply to prospects** | The contact form emails submissions to `doortodelicious@gmail.com`. There is **no** AI auto-responder. | ✅ Compliant. **Do not** add an AI auto-reply, chatbot, or AI-written "reply as Karen". Karen answers enquiries personally. No AI-generated testimonials or reviews anywhere on the site. |
| **Can #1 — identify by role** | "Independent Thermomix® Consultant" is shown prominently. | ✅ Compliant. |
| **Can #6 — approved visuals only** | See Cannot #4 action above. | ⚠️ Pending asset confirmation. |

---

## §3a — Open items for Karen to confirm (recommended page `/`)

- **Surname in public:** the page now uses "Karen Skarda" (from the redesign brief).
  Confirm she wants her full name on the site.
- **Disclaimer wording / trademark holder:** footer reads "Thermomix® and Cookidoo®
  are registered trademarks of Vorwerk. … not published by, endorsed by, or directly
  affiliated with Vorwerk LLC." Confirm the exact entity name Thermomix wants
  (Vorwerk / Vorwerk LLC / Vorwerk SE & Co. KG) against her current consultant agreement.
- **Model name:** page and FAQ say "the current flagship is the Thermomix® TM7."
  Confirm that matches current US availability.
- **Images:** hero and "Meet Karen" use placeholders (a food photo + a "photo coming
  soon" block). Karen should supply her own lifestyle/kitchen photo and a portrait.
  Do not substitute Thermomix marketing creatives (`assets/thermomix.jpg` is not used
  on this page — see Cannot #4).
- **Cookidoo®** is now referenced (guided cooking). Fine as a real Vorwerk product;
  keep the ® and the trademark line.

## §4 — Standing rules for future edits

- Write **Thermomix®** with the ® symbol on prominent uses.
- Never imply the site is operated by, affiliated with, or endorsed by Vorwerk /
  Thermomix USA / Vorwerk LLC. Keep the footer disclaimer on every page.
- **No trademark** ("thermomix", "thermo", or lookalikes) in the domain, site
  name, page titles, or social handles linked from the site.
- **No on-site cart, pricing, or checkout.** Orders go through
  `shop.thermomix.com/consultant/109102`.
- **No personalized incentives** ("gift card", "free gift", "$X when you order
  through me", "exclusive bonus from me"). Describe only the standard/national
  offer, with no specific dollar figure unless official materials use it.
- **No income, earnings, or lifestyle claims**; no consultant-recruitment content.
- **Only approved/authorized brand images.** Prefer Karen's own photos. Do not add
  Thermomix logos, marketing creatives, or product footage that aren't on the
  approved-assets list.
- **No DIY assets for national offers** (financing, bundles, price promos).
- **AI-assisted copy must be reviewed, personalized, fact-checked, and approved by
  Karen** before it ships under her name.
- **No AI auto-reply, chatbot, or AI-written testimonials/reviews** on the site.
  Enquiries are answered personally.
- Keep "Independent Thermomix® Consultant" near the top of every page and in the footer.
