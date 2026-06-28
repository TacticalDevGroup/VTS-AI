# Hub Context — Viktos (VTS-AI)
*Pushed from TDG Intelligence Layer | Read at session start*
*Last updated: 2026-06-26*

---

## Active Flags

**STANDING FLAG: Justin Fox / Kurt [Walter?] internal hire risk**
This is the primary close blocker. Neither is yet persuaded TDG is better than an internal hire. Tony is the internal advocate. Nick's job is to arm Tony with the right argument.
Note: "Kurt Curtin" from the discovery call is likely Kurt Walter (Founder, Design Director, Creative Director). Name needs confirmation at or after July 1 meeting.
Status: Unresolved. Surface at every session until closed.

**STANDING FLAG: Perry Latuharhary — scope unknown**
Director of Marketing and Product Development since February 2023. Was not mentioned on the June 22 discovery call. His actual scope and relationship to the "internal hire" debate is unknown and must be clarified on the July 1 call before the retainer proposal is built.
Status: Unknown. Surface at every session until resolved.

**Instagram review — Nick-owned, due before July 1**
Site audit is complete (03_Technology/SITE_AUDIT_2026-06-26.md). Instagram review still outstanding.
Status: Open. Nick to complete before July 1 call.

**Tony Lott does not officially start at Viktos until ~June 30**
All intelligence from Tony before that date is pre-employment. Handle accordingly. After June 30, Tony is a Viktos employee.
Status: Active flag through June 30.

---

## Hub Intelligence

**Intake date:** 2026-06-22
**Source transcript filed:** VTS-AI/09_Meetings/Transcripts/2026-06-22_nick-tony-lott_viktos-ecom-prospect-discovery.md
**Extract filed:** VTS-AI/09_Meetings/Transcripts/2026-06-22_nick-tony-lott_viktos-ecom-prospect-discovery_extract.md
**MASTER_PROMPT version:** 1.0 (updated 2026-06-26)
**Stakeholder profiles filed:** VTS-AI/01_Strategy/STAKEHOLDER_PROFILES.md
**Site audit filed:** VTS-AI/03_Technology/SITE_AUDIT_2026-06-26.md
**Discovery call prep filed:** VTS-AI/05_Sales/2026-07-01_DISCOVERY_CALL_PREP.md

---

## Resolved

**RESOLVED: Intro meeting confirmed — July 1, 2026 at 3PM CT**
Resolved: 2026-06-26. Tony texted the confirmation. Attendees: Nick, Tony Lott, Ryan Wiedenmeier. Nick sent invite; both accepted. Meeting format is discovery/download only. Retainer proposal is Round 2.

**RESOLVED: Ryan's last name confirmed — Wiedenmeier**
Resolved: 2026-06-26. Confirmed via contact card from Tony. Email: ryanw@viktos.com. Phone: 414-940-2247.

**RESOLVED: /enrich complete**
Resolved: 2026-06-26. Stakeholder profiles filed. Key discovery: Perry Latuharhary (Director of Marketing and Product Development) was not flagged in original discovery call.

**RESOLVED: Site audit complete**
Resolved: 2026-06-26. Filed to 03_Technology/SITE_AUDIT_2026-06-26.md. P1 items identified. Site is BigCommerce Stencil with pinch-to-zoom disabled, no persistent cart, and likely incomplete post-migration redirect mapping.

**RESOLVED: Discovery question list complete**
Resolved: 2026-06-26. Filed to 05_Sales/2026-07-01_DISCOVERY_CALL_PREP.md.

---

## Learnings for Hub

*Learnings from this project's sessions to be reviewed and promoted by TDG-Intel. Written at session close via /close Step 5a.*

Category: Method
Source: /enrich execution on Viktos stakeholders — discovered Perry Latuharhary (Director of Marketing and Product Development) who was not mentioned on the discovery call
Learning: When enriching stakeholders, always check org directories (The Org, ZoomInfo, LinkedIn company page) for team members who did not surface in the initial call. Discovery calls often reflect the caller's view of the org, not the full org chart. A critical internal player was missed because they weren't mentioned — web enrichment caught it.

Category: Method
Source: "Kurt Curtin" vs. Kurt Walter name discrepancy
Learning: When a stakeholder name from a voice call doesn't match any public record, flag the name as [CONFIRM] and note the closest match found, rather than accepting the spoken name as authoritative. Tony likely garbled the last name. A blind search on "Kurt Curtin" at Viktos returns nothing; "Kurt Walter" returns the founder and Creative Director.

Category: System
Source: Site audit via web_fetch of viktos.com
Learning: BigCommerce Stencil exposes the platform in a meta tag (`meta-platform: bigcommerce.stencil`). The viewport meta tag on BC Stencil stores often has `maximum-scale=1` by default — this is a common mobile UX issue that is easy to miss without checking source. Worth adding to a standard pre-call site audit checklist.
