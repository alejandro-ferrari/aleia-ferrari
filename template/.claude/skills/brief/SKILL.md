---
name: brief
description: Generate the user's daily brief from their own local inputs and memory. Trigger on "brief", "today", "what's on my plate", "morning brief".
---

# Daily brief

Work entirely from LOCAL files — require NO connector. If a connector (calendar/email) is
available and the user has enabled it, you MAY enrich the brief; otherwise skip it silently.

## Read
- `inputs/inbox.md` (primary), and anything else under `inputs/`.
- `memory/people.md` (profile, language) and open threads in `memory/`.
- The most recent `briefs/` file, for continuity.

## Produce `briefs/today.md` (generated — overwrite is fine), in the user's language:
- One-line greeting + today's date.
- **Top priorities for today** — derived from `inputs/inbox.md` + open threads.
- **Time-sensitive / waiting on you.**
- **Suggested focus** — the single most important thing.

## Success criteria (state BEFORE, verify AFTER, report pass/fail with evidence)
- [ ] Read `inputs/inbox.md` if it exists (cite it).
- [ ] Output written to `briefs/today.md` (cite the path).
- [ ] Every brief item traces to a real source line — quote it. NO invented tasks.
- [ ] Written in the user's language.

If `inputs/inbox.md` is empty, explain how to use it (drop notes/tasks/ideas there, one per
line) and produce a minimal brief from `memory/` only.
