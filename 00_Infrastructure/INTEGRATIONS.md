# Integrations — Viktos (VTS-AI)
*Last updated: 2026-06-22*
*Classification: TDG Internal*

---

## Current Tech Stack (As Known)

| Platform | Status | Notes |
|---|---|---|
| BigCommerce | CONFIRMED | Core ecommerce platform. Migrated from Shopify January 2025. |
| NetSuite | CONFIRMED | ERP/back-office. |
| Klaviyo | LIKELY | Inferred from BigCommerce ecosystem; not confirmed on call. |
| Instagram | CONFIRMED | 206K followers. Direct API connection possible for analytics. |
| Zapier | UNKNOWN | May be in use; not discussed. |

*Full tech stack confirmation needed via /enrich or stakeholder interview at team meeting.*

---

## Connector Roadmap (Target State)

| Connector | Priority | Path | Blocker |
|---|---|---|---|
| BigCommerce MCP | HIGH | Native or ABT build | Engagement must start first |
| Klaviyo MCP | HIGH | Native connector available in Cowork | Confirm Klaviyo is in use |
| Google Analytics 4 | HIGH | ABT or native | GA4 property access grant needed |
| Instagram API | MEDIUM | Meta Graph API | Access grant + app setup |
| NetSuite | MEDIUM | Custom build (ABT) | Complex ERP; scope after Phase 1 |
| Monday.com / Asana | LOW-MEDIUM | TBD | Depends on what Viktos uses for PM |

---

## Phase 1 Connector Priority

Before connectors are built, the intelligence layer starts with files and documents (knowledge base). Phase 1 connectors add live data access.

Recommended Phase 1 connectors (post-engagement start):
1. BigCommerce: product catalog, order data
2. Klaviyo (if confirmed): email performance
3. GA4: web analytics

---

## Notes

- No connector build begins until the engagement is formally started (SOW executed)
- Tony Lott is the gatekeeper for any access grants at Viktos
- NetSuite integration is a Phase 2+ item; scope and complexity TBD
