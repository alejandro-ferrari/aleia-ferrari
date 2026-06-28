---
name: doctor
description: Check the health of the Aleia Ferrari install — required files, version, profile, drift. Trigger on "doctor", "check", "is everything ok", "diagnóstico".
---

# Doctor — health check

Check and REPORT (do not fix without asking). Reply in the user's language as a short
checklist: ok / missing / suggested action.

- Required files present: `CLAUDE.md`; `.claude/skills/` with `aleia-onboard`, `brief`,
  `plan`, `update`, `doctor`; `inputs/inbox.md`; `memory/people.md`; `.aleia/version.json`.
- Installed version (from `./.aleia/version.json`). Offer to run the `update` skill to check
  for a newer one.
- Profile: does `memory/people.md` have confirmed fields? If empty → suggest onboarding.
- Anything missing, empty, or obviously broken.

End by offering the matching skill to fix what's flagged (onboarding / update). Never modify
`inputs/` or `memory/` here.
