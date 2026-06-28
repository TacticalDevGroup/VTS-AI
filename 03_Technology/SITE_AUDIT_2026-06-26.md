# viktos.com Mobile Site Audit
*TDG Intelligence Layer | VTS-AI*
*Audit date: 2026-06-26 | Auditor: TDG (Claude)*
*Platform confirmed: BigCommerce Stencil*
*Classification: TDG Internal*

---

## Summary

Viktos runs on BigCommerce Stencil. The site has identifiable mobile UX issues that directly explain the conversion gap on what Tony confirmed is 70-80% mobile traffic. The most critical issues are (1) a disabled pinch-to-zoom viewport setting, (2) sale prices that are hidden until cart, and (3) no persistent cart or cart abandonment recovery visible. The post-migration SEO damage from the January 2025 Shopify to BigCommerce switch is likely ongoing and unaddressed.

This audit is based on HTML/rendered content analysis. A live device walkthrough and Google Search Console/GA4 access will be needed for a full post-mortem.

---

## Mobile UX Issues

### 1. Pinch-to-Zoom Disabled (High Impact)

Every page on viktos.com includes this viewport meta tag:
```
meta-viewport: width=device-width, initial-scale=1, maximum-scale=1
```

`maximum-scale=1` disables pinch-to-zoom on iOS and Android. For a tactical apparel brand where buyers want to examine stitching, materials, pockets, and functional details, this is a direct conversion killer. A mobile user cannot zoom into a product image. This also violates WCAG 2.1 accessibility guidelines and could affect search rankings.

**Fix:** Remove `maximum-scale=1` from the viewport meta tag. This is a one-line theme edit in BigCommerce Stencil.

---

### 2. Sale Prices Hidden Until Cart (High Impact)

The homepage displays a persistent banner: "Sale Prices Reflected In Cart."

This means a mobile shopper browsing sale items cannot see their actual price until they add to cart. This creates three problems: (a) shoppers bounce rather than add to discover price, (b) it erodes trust ("why is the price hidden?"), and (c) it inflates cart abandonment because price discovery happens at the cart rather than the product page.

The product pages (e.g., Counteract 27 Backpack) do show the sale price directly ($115 vs. $195 original), so the issue may be specific to collection/browse pages or a sale-event configuration rather than a sitewide setting. Needs validation against collection page behavior.

**Fix:** Ensure sale prices are displayed in-line on collection and search result pages. This is a theme-level fix in BigCommerce Stencil.

---

### 3. No Persistent Cart (High Impact — Tony's #1 Call-Out)

No persistent cart functionality is evident on the site. The cart.php page returned an empty response. BigCommerce does support persistent cart (Stencil has this as a feature), but it requires enabling in store settings.

Persistent cart means a customer's cart is saved across sessions and devices. Without it, a mobile user who adds items but doesn't checkout loses their cart when they close the browser. With 70-80% mobile traffic, this is a significant revenue leak.

Cart abandonment email/SMS recovery (Klaviyo) is likely not configured, or configured without persistent cart support. This means the recovery flow is operating against a broken foundation.

**Fix:** Enable persistent cart in BigCommerce Store Settings. Confirm Klaviyo cart abandonment flows are active and connected.

---

### 4. Mobile Navigation Complexity (Medium-High Impact)

The site has 12 top-level navigation categories, each with 8-10 sub-items, plus a "New and Featured" section that repeats across every category dropdown. On mobile, this renders as a hamburger menu that expands into a deeply nested structure.

For a mobile shopper in discovery mode, this is overwhelming and hard to navigate quickly. The current structure was designed for desktop; it has not been simplified for the mobile experience that represents the majority of traffic.

**Fix:** Redesign the mobile nav to lead with top sellers, featured collections, and category-level landing pages. Reduce nesting. A single "Browse All" or "Shop by Category" layer is more mobile-appropriate.

---

### 5. No Email or SMS Capture on Homepage (Medium Impact)

The homepage has no visible email opt-in or SMS capture mechanism. For a brand relying on Klaviyo (assumed from BigCommerce ecosystem norms) to drive repeat purchases and cart recovery, no email capture means every new organic visitor who doesn't convert is permanently lost.

Given the organic traffic weakness Tony described, the first-party data capture gap is compounding the acquisition problem. Even visitors who don't buy should be entering the Klaviyo flow.

**Fix:** Add a homepage email/SMS pop-up or inline opt-in with a first-purchase incentive. This is a Klaviyo popup, easy to deploy without a developer.

---

### 6. About Page is Thin (Medium Impact — New Customer Acquisition)

The About page is a single paragraph:
> "VIKTØS was launched in the fall of 2017 by a combined force of industry and military veterans; our mission is to produce innovative gear for the tactical user. Our product transcends the typical boundaries of conventional tactical companies and addresses the entire black gun lifestyle, from combat to training and everyday carry to R&R."

No founder story. No mention of Jeff Fox. No veteran operator testimonials. No brand mission narrative. For a brand whose core conversion argument is "designed by people who actually use this gear," the About page is leaving significant emotional and credibility value on the table.

Justin Fox's founder story (family business, military roots, his father, the black gun lifestyle) is a compelling brand narrative. First-time visitors — especially those coming from social and discovering the brand for the first time — have no reason to trust the brand beyond the product itself.

**Fix:** Rewrite the About page with a full brand story. This is a content project, not a technical one.

---

### 7. Product Page Variant Selection UX (Medium Impact)

On the Counteract 27 Backpack product page, the color selector reads "Color: (Required) / Selected Color is [blank]." The Add to Cart button is visible but color must be selected first. On mobile, this creates confusion — the button appears actionable but the cart won't accept the item until a color is selected, and the visual feedback for that requirement is unclear.

**Fix:** Make the first available variant auto-selected on page load, or use a clearer mobile-friendly variant selector (swatches instead of dropdown).

---

### 8. Product Reviews Are Thin (Low-Medium Impact)

The most visible product on the homepage (Counteract 27 Backpack, featured at 41% off) has only 5 reviews, with a mixed 4-star average and one detailed negative review about comfort and main compartment usability. On mobile, this is often the first trust signal a browser will look for after price.

The brand's products are likely better-received than the review counts suggest — this is a review generation problem, not a product quality problem.

**Fix:** Deploy a post-purchase email review request sequence in Klaviyo. Target existing customers first to build baseline review counts on top SKUs.

---

## SEO Observations

### Post-Migration Damage (High Impact — Requires Data Access)

The January 2025 Shopify to BigCommerce migration is the most likely cause of the organic traffic collapse. Shopify and BigCommerce use different URL structures:

- Shopify: `/products/[product-name]` and `/collections/[collection-name]`
- BigCommerce: `/[product-name]/` and `/[category-name]/`

If 301 redirects were not comprehensively mapped from every indexed Shopify URL to its BigCommerce equivalent, Google's crawl would have surfaced thousands of 404s. This triggers a significant rankings loss, typically taking 6-18 months to recover organically even after the redirects are fixed.

The internal team that executed the migration is still at Viktos. Their account of what was done with redirects should be verified independently against Google Search Console data.

**What TDG needs to assess:** Access to Google Search Console (impressions/clicks before and after January 2025), GA4 traffic data pre/post migration, crawl error logs, and the redirect map used during migration (if one exists).

---

### Homepage Meta Description (Low-Medium Impact)

Current: "Building gear for your daily gunfight: Apparel, shoes, boots, gloves and bags crafted for tactical necessity. Concealed carry or open we live the black gun lifestyle"

This is brand voice language, not keyword-optimized copy. It doesn't target any high-intent search query (e.g., "tactical pants," "CCW backpack," "concealed carry jeans"). The homepage meta description surfaces in Google search results and is a first-impression conversion element for organic traffic.

**Fix:** Rewrite to lead with one or two high-volume target keywords, then brand differentiation. Example: "Shop tactical apparel, CCW gear, and footwear designed for operators and everyday carry — built by US veterans for the black gun lifestyle."

---

### Product Pages: Title Tag Pattern is Reasonable

Example: "Counteract 27 Backpack | Modular Concealed Carry Backpack | VIKTOS"

This pattern hits relevant keywords (concealed carry backpack) and includes the brand name. Product page SEO is more functional than homepage SEO. The issue is more likely at the category/collection level and from migration redirect gaps.

---

### Competitor Context

Per SimilarWeb (August 2024 data, directional only): Viktos's top comparable site is vertx.com (223K monthly visits). Much larger players like 511tactical.com (2M visits) and primaryarms.com (3.1M visits) occupy adjacent but different market positions. Viktos's niche (gray man, CCW lifestyle, consumer-facing) is differentiated. The SEO gap is recoverable given that the niche is less competitive than broad tactical retail.

---

## Tech Stack (Confirmed and Inferred)

| Platform | Status | Notes |
|---|---|---|
| BigCommerce Stencil | CONFIRMED | Meta tag: bigcommerce.stencil. Active theme with standard Stencil structure. |
| Klaviyo | LIKELY (unconfirmed) | Industry norm for BigCommerce stores; no confirmation from page source |
| Google Analytics / GA4 | LIKELY | Standard BC integration; not confirmed from page source |
| Google Ads pixel | UNKNOWN | Needs Google Tag Manager audit |
| Microsoft/Bing pixel | UNKNOWN | Tony flagged this as a Ryan priority |
| NetSuite ERP | CONFIRMED (discovery call) | Back-office; not visible from site |
| YKK Zippers, Tuff Hyde | Vendor | Product material callouts on product pages |

---

## Priority Fix List

| Priority | Issue | Fix Type | Effort |
|---|---|---|---|
| P1 | Persistent cart not enabled | Settings toggle in BC | Low |
| P1 | Pinch-to-zoom disabled | One-line theme edit | Low |
| P1 | Post-migration redirect audit | Technical SEO + GSC access | Medium |
| P2 | Sale prices hidden until cart | Theme/logic fix | Medium |
| P2 | Email/SMS capture on homepage | Klaviyo popup | Low |
| P2 | Mobile navigation redesign | Theme + UX | Medium |
| P3 | About page rewrite | Content | Low |
| P3 | Product variant UX | Theme edit | Low |
| P3 | Review generation program | Klaviyo flow | Low |
| P3 | Homepage meta description | Content | Low |

---

## What TDG Cannot Assess Without Access

- Google Search Console: indexed page counts, 404 error volumes, impressions/clicks before and after January 2025
- GA4: traffic source breakdown, mobile conversion rate, bounce rate by device
- Klaviyo: flow status, list size, email capture rate, cart abandonment recovery rate
- BigCommerce admin: persistent cart setting, redirect log, app integrations
- Google Tag Manager: what pixels are actually firing and on which pages

These data points are the foundation of a credible post-mortem. The July 1 call should establish access or a path to access.

---

*Filed: VTS-AI/03_Technology/ | TDG Internal*
