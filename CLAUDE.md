# Viktos (VTS-AI) — Session Auto-Brief
*TDG Intelligence Layer | Auto-executes at session start*

## On Every Session Open

Before responding to any user input, execute this sequence in order:

1. Read `_hub-context.md` (if exists) — read first: time-sensitive flags take priority
2. Read `00_Infrastructure/MASTER_PROMPT.md`
3. Read `00_Infrastructure/_project-status.md` (if exists)
4. Read `00_Infrastructure/_active-threads.md` (if exists)
5. Read `00_Infrastructure/DECISIONS_LOG.md` (full file, if exists)
6. Deliver a structured opening brief: current prospect status, last known touchpoint, open items, immediate priorities, and any hub flags

Do not wait to be asked. Do not ask what Nick wants to work on. Open with the brief.

---

## Standing Rules

**Volatile state:** Read source files before acting on any status claim. Never rely on memory alone for project facts.

**Em dash rule:** Never use em dashes in any output. Use commas, colons, parentheses, or restructured sentences.

**Outbound comms:** Never send anything externally. Nick approves every send.

**Data governance:** VTS Tier 1 data never leaves this project folder.

**Primary champion:** Tony Lott. He does not officially start at Viktos until approximately June 30, 2026. All intelligence from Tony before that date is pre-employment and should be handled with appropriate discretion. Never reference Tony as a source in any prospect-facing materials.

**Ryan's last name:** Not confirmed. "Ryan Meyer" or "Ryan Miller" were both referenced. Flag as [CONFIRM] until verified at the team meeting.

**Justin Fox and Kurt Curtin:** Both potentially prefer an internal hire over TDG. This is the primary close risk. Surface it at every session until it is resolved.

**Option B:** The reduced base plus uncapped performance comp option mirrors Tony's own comp structure. Keep this positioning consistent across all materials.

**TDG role:** Nick is CMO/CTO function, not a developer. Frame all recommendations accordingly. Development goes to Nick's network.

**GTD crossover:** None. Do not recommend Viktos placement at GT Distributors.

**_TDG_Internal/STRATEGIC_ASSESSMENT.md:** TDG-internal only. Never surface in prospect-facing materials.

**Interim decision recognition protocol:** During any working session, actively monitor for decisions being made. Decision signals include: "let's go with," "confirmed," "that's the plan," "we're doing X," resolving an open question, agreeing to a recommendation, locking in a timeline or sequence. When a decision signal is detected, surface a short list for Nick's review before writing anything to the log: "Decisions I'm seeing this session — confirm to log: [list]." Nick confirms, modifies, or removes items. Only confirmed decisions are written to DECISIONS_LOG.md.

**Conflict detection and routing:** When work in this session touches a topic that belongs in a different project, flag it immediately: "This belongs in [project] — should I open that context or note it here for routing?" Do not silently absorb cross-project work into the wrong session. Route confirmed items to the correct project layer before this session closes.
