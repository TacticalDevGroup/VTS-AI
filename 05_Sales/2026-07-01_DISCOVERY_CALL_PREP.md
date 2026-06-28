# July 1 Discovery Call Prep — Viktos
*TDG Intelligence Layer | VTS-AI*
*Call: July 1, 2026 at 3PM CT*
*Attendees: Nick Hoffman (TDG), Tony Lott (VP Commercial Ops), Ryan Wiedenmeier (GM)*
*Mode: Nick in discovery / download. NOT a pitch. Retainer proposal is Round 2.*
*Classification: TDG Internal*

---

## Call Objectives

1. Give Ryan a full picture of TDG's capabilities against his stated pain points (BigCommerce, Google Marketing, tracking pixels, organic traffic, mobile, SEO).
2. Get a complete download on what the team actually needs — Ryan's version, not Tony's secondhand version.
3. Surface the Perry Latuharhary question without triggering defensiveness (what is the current marketing structure?).
4. Establish access path to the data TDG needs: GSC, GA4, Klaviyo, BC admin.
5. Understand Justin Fox's involvement — when does he enter the process?
6. Give Tony something to point to when he makes the case internally.

---

## Nick's Opening Frame (30 seconds)

Tony asked me to come in ready to listen before I talk. So that's what I'll do — I want to understand what you're dealing with before I tell you how TDG approaches it. I've spent time on the site this week and I have observations, but your read from inside the business matters more than what I can see from the outside. Let's start there.

*(This opening does two things: signals discovery mode, and frames the site audit observations as a follow-on — not a cold pitch.)*

---

## Discovery Questions

### Current State and the Migration

1. When you look back at January 2025 — the Shopify to BigCommerce migration — what's your honest read on how it went? And how much of the traffic and revenue loss do you feel like you've recovered since then?

2. Who ran the migration internally? Are they still with you? *(Understand whether the people who built the problem are still managing it.)*

3. Do you have access to Google Search Console? What does the impression/click data tell you before versus after the migration? *(If they don't know, that's a finding.)*

4. When you say organic traffic is weak — is that a baseline-weak problem (never had strong organic) or a post-migration problem (had it and lost it)? *(Critical distinction for how TDG scopes the fix.)*

---

### Mobile and Site Performance

5. You mentioned 70-80% of your ecom traffic is mobile. What's your current mobile conversion rate — do you have that number off the top of your head? *(Expected: they don't. This opens the GA4 access conversation.)*

6. The persistent cart issue Tony flagged — is that a known gap in your current BigCommerce setup, or has someone tried to address it and hit a wall?

7. Who manages the site day to day? Is that internal, or through a BigCommerce developer or agency?

---

### Customer Acquisition

8. When you say new customer acquisition is weak — where are new customers actually coming from right now? Organic search, paid search, social, direct? *(Get them to describe their channel mix.)*

9. Are you running any paid search right now — Google or Bing? If so, who manages it?

10. What does your email or SMS program look like? Are you on Klaviyo? What's your list size, roughly? *(Validates the Klaviyo assumption and reveals first-party data health.)*

---

### SEO and Keywords

11. Tony mentioned generic keywords as a problem. Do you have a sense of what terms you're actually ranking for versus the terms your customers are searching when they find competitors? *(Probably not — this surfaces the need for an SEO audit.)*

12. Have you done any SEO work since the migration? Any agency or freelancer handling it, or has it been internal?

---

### Team and Structure (Handle with Care)

13. How is marketing structured right now? Who owns it day to day? *(Opens the Perry Latuharhary question without naming him. Let Ryan describe the structure.)*

14. What would the ideal outcome look like for you — more internal headcount, external support, or some combination? *(Get Ryan's own words on the internal-hire-vs-agency debate.)*

---

### Tracking and Attribution

15. What tracking do you have in place right now — Google Analytics, Google Ads pixel, Microsoft Ads pixel? Do you know if they're firing correctly across the site? *(Ryan is IT-savvy; this is in his wheelhouse. Establishes TDG's technical credibility when Nick follows with attribution context.)*

16. Do you have any attribution model in place — meaning, do you know which channels are actually driving revenue versus assisted conversions?

---

### BigCommerce and Tech Stack

17. Are you using any BigCommerce apps for cart abandonment, reviews, or upsell — or is the store running fairly vanilla out of the box?

18. NetSuite is your ERP — is that integration with BigCommerce working cleanly, or is there friction there?

---

### Access and Next Steps

19. To put together a meaningful analysis and proposal, I'm going to need eyes on some data. Who would need to grant access to Google Search Console, GA4, and BigCommerce admin — is that you, or does that need to go through someone else?

20. Justin isn't on today's call. What's the right way to get him into the conversation once we have a proposal ready? *(Surfaces the decision-making path without making it awkward.)*

---

## What NOT to Do on This Call

- Do not pitch retainer options. That is Round 2.
- Do not lead with the site audit. Use it as a proof of diligence after you've gotten Ryan's download.
- Do not name Perry Latuharhary unless Ryan brings him up.
- Do not reference Tony as the source of any specific pain point intel. Let Ryan describe problems in his own words.
- Do not propose timelines or budgets. You don't have enough information yet and it's too early.

---

## TDG Capability Proof Points (For When Ryan Asks)

Tony said Ryan will want to hear capabilities across these areas:

**BigCommerce:** TDG has worked in the BigCommerce ecosystem. We understand Stencil themes, BC's native SEO structure, persistent cart, app integrations, and the redirect/migration framework. We know where migrations break and how to fix them. *(Credibility point: "We've done post-mortems on BigCommerce migrations specifically.")*

**Google Marketing (Search and Shopping):** TDG manages paid search and Shopping campaigns in Google Ads. We understand smart bidding, product feed optimization for BigCommerce-to-Google sync, and campaign structure for DTC apparel.

**Google Ads and Microsoft Ads Tracking Pixels:** TDG audits and implements tracking pixels through Google Tag Manager. We verify that pixel events are firing correctly, that conversion windows are set properly, and that remarketing audiences are building. This is a first-week deliverable — we don't wait to get attribution right.

**Organic Traffic Recovery:** Post-migration organic traffic loss follows a predictable playbook: 301 redirect audit, crawl error remediation, sitemap resubmission, content consolidation, and keyword gap analysis. TDG has done this. The data access request (GSC, GA4) is what unlocks the post-mortem.

**Attribution:** TDG's attribution model is a differentiator. Most brands don't know which channels are actually driving revenue — they know last-click, not the full path. We build multi-touch attribution into the reporting foundation.

---

## Observations Nick Can Deploy (After the Download)

These are from the site audit. Use them to demonstrate you've done your homework, not to lead with.

- The viewport `maximum-scale=1` setting is disabling pinch-to-zoom on mobile — that's a known mobile UX issue and a one-line fix in Stencil.
- Sale prices being hidden until cart creates friction for mobile shoppers who want to know what they're actually paying before they commit.
- The persistent cart is not enabled — this is a settings toggle in BC admin, not a development project.
- The About page is a missed conversion opportunity — the brand has a compelling founder story that isn't being told.
- Review counts are thin on top SKUs, which affects conversion for new visitors.

---

## Red Flags to Listen For

- If Ryan describes the migration as "basically fine" — the internal team is defensive. Proceed carefully.
- If Ryan doesn't know mobile conversion rate — GA4 access isn't being used. That's a larger attribution problem.
- If Perry Latuharhary is described as owning ecom — TDG is not filling an empty seat. Understand the scope before the proposal.
- If Ryan signals Justin Fox needs to be in the loop before any access is granted — the decision authority is not at Ryan's level. Adjust the proposal approach.

---

## Post-Call Immediate Actions

1. Send Ryan a brief follow-up with a summary of what was discussed and the data access request (GSC, GA4, BC admin, Klaviyo).
2. Update Tony on how the call went and what Ryan's actual temperature is.
3. Log decisions, new intel, and any updated close risk flags.
4. Begin drafting Option A and Option B retainer proposals.

---

*Filed: VTS-AI/05_Sales/ | TDG Internal*
