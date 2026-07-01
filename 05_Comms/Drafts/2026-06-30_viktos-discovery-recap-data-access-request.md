# Viktos x TDG: Discovery Call Recap + Data Access Request
*Draft for Nick review | 2026-06-30 | Send to: Ryan Wiedenmeier, Tony Lott*

---

**Subject:** [Viktos] x TDG: Call Recap + Data Access

Ryan, Tony,

Appreciate the time today. Quick recap of what I heard and where I'd start.

**What I'm seeing:**

The BigCommerce migration in January created a traffic bleed you're still working through. Broken 301s and 404s are the primary culprit, and Ryan, you're already in GSC working the audit. The good news: three of the highest-impact issues I spotted are admin-level fixes, not development projects.

- **Persistent cart** is almost certainly a native BigCommerce setting. If it's disabled, every session that ends without a purchase loses the cart. On 75% mobile traffic, that's a daily revenue leak with a 15-minute fix.
- **Pinch-to-zoom** is a single line in the viewport meta tag. Mobile users can't examine product detail. One change.
- **301 redirect completion** will recover organic traffic you're still losing. Ryan, once the crawl settles, we'll know the scope.

Beyond those: the site is visually strong but not optimized for purchase flow. Above-the-fold CTA placement, add-to-cart prominence, and Tag Manager accuracy (if tracking is off, PPC bids are running against bad data) are the next layer.

Klaviyo is in place. I want to see the automation flows, conversion rates, and what the messaging looks like before forming an opinion on email.

One more thing worth flagging now, because it's a fast win once we have access: I looked at the Instagram feed. You've got 206,000 followers and posts that pull 1,000 to 2,000 likes when they're in culture mode (the John Wayne, Heat, Optimus Prime content), but product posts are landing at 40 to 100 likes. That's not a content execution problem, it's a strategy problem, and it's a good one to have, because the audience is already telling you what it responds to. Closing that gap between cultural engagement and product engagement is a high-leverage, low-cost first move once we're inside the account.

**What I need to get started:**

To validate what I'm seeing and build a proper diagnostic, I'd like access to:

- Google Search Console
- Google Analytics 4
- BigCommerce Admin (read access)
- Google Tag Manager
- Klaviyo (reporting/flow view)

If you can add nick@tacticaldevgroup.com as a user in each, I'll have a full picture within a few days and can come back with a prioritized list.

**Next step:**

I know Justin wasn't on today's call. Happy to connect with him whenever it makes sense, walk through what I'm seeing, and talk about what the right scope looks like. No rush on that, but I want to make sure he has eyes on this directly.

Talk soon.

Nick
nick@tacticaldevgroup.com | 612.770.9566
