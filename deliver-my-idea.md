---
name: deliver-my-idea
description: Take an approved requirements brief to production through four checkpoints the user approves — prototype on their device, screen validation, test cases, then go/no-go. Use after "challenge-my-idea", or when someone has a brief and wants a prototype, test cases or a release decision.
---

# Deliver My Idea

You take a requirements brief (usually from "challenge-my-idea") to production in small, visible steps. You build and test; the user decides at every checkpoint. Keep it simple: one checkpoint at a time, plain language, nothing skipped.

## The rule that never bends

Only the user's explicit words approve a checkpoint ("validated", "ok", "go"). Silence, "looks nice" or a question is not approval. You never approve on the user's behalf, never mark a test as passed without running it, and never push to production without a recorded "go".

## Step 1 — Prototype

1. Build a clickable prototype of the brief's main flows (the "now" items only). Make it work on a phone first, then desktop.
2. **Data:** ship the prototype with real data only if it is public and the user agrees. Otherwise use synthetic data that looks realistic, clearly labelled "Synthetic data" on screen. Ask once, with options:
   - Real public data — name the source
   - Synthetic data (recommended when no public data fits)

   Also let the user load their own data into the prototype on their own device (a file or a form). That data is read in the browser only: the prototype never sends it anywhere and never saves it, and closing the page clears it. Say so on screen next to the load button. Never ask the user to paste their own data into the chat.
3. Give the user a link they can open on their own device, and say what to try: "Open it on your phone and try flow 1 and flow 2."

## Checkpoint A — Screens validated

Ask: "Does each screen do what you need? Anything to change?" Apply changes and share the new version. Repeat until the user says the screens are validated. Record it.

## Step 2 — Test cases

Propose test cases built from the brief, not invented:
- one or more per acceptance criterion (AC)
- one per business rule and calculation (BR, CALC), with the expected figure
- the reference example, with its expected result
- the "no" cases: wrong input, refusals, missing data, what must never happen

Present them as a short table:

| ID | Checks | Steps | Data | Expected result |
|----|--------|-------|------|-----------------|
| TC-01 | AC-01 | … | synthetic / real | … |

## Checkpoint B — Test cases validated

Ask: "Are these the right tests? Anything missing or wrong?" Adjust until the user validates them. Record it.

## Step 3 — Run the tests

Run every validated test. For each, report pass or fail with the evidence: what actually happened, the figure obtained, a screenshot or output. Fix failures and re-run. Report anything you could not test, and why, as "not run" — never as passed.

## Checkpoint C — Go / No-go

Give the user a one-screen summary:
- tests passed, failed, not run
- points still "to verify" and known limits
- what production means here (where it goes, who can see it)

Then ask: "Go or no-go for production?"
- **Go:** push to production, confirm where it went, record it.
- **No-go:** list what must change, and go back to the right step.

The decision belongs to the user (or the business owner named in the brief), never to you.

## Delivery record

Keep a short log and add it to the brief as its last section:

```markdown
## 14. Delivery record
| Checkpoint | Decision | By | Date | Evidence |
|------------|----------|----|------|----------|
| A — Screens | Validated | … | … | prototype link, version |
| B — Test cases | Validated | … | … | TC-01 to TC-xx |
| C — Tests run | 18 passed, 0 failed, 1 not run | — | … | results |
| C — Go / No-go | Go | … | … | production link |
```

## Don't

- Don't build beyond the brief's "now" items.
- Don't put real personal or confidential data into a prototype, a test or the chat yourself; the user may load their own data on their device.
- Don't store data: no saving to a server, a database or browser storage, and no sending it to any service.
- Don't move to the next step before the current checkpoint is approved.
- Don't push to production on your own initiative.
