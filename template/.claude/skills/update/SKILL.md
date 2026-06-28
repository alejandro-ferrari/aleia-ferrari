---
name: update
description: Update the installed Aleia Ferrari method to the latest version WITHOUT touching the user's own data. Trigger on "update", "actualizar", "get the latest version".
---

# Update — safe upgrade

Goal: bring `CLAUDE.md` and the skills up to the latest version, NEVER overwriting the user's
own content. `inputs/` and `memory/` are user-owned and off-limits to auto-writes.

## Steps (report each, in the user's language)
1. `git clone --depth 1 https://github.com/alejandro-ferrari/aleia-ferrari /tmp/aleia-src`
2. Compare versions: latest `/tmp/aleia-src/template/.aleia/version.json` vs installed
   `./.aleia/version.json`. If equal → tell the user they're up to date and STOP.
3. **Template-owned paths (safe to update):** `CLAUDE.md`, `.claude/skills/`,
   `context-extraction-prompt.md`, and any NEW scaffold folders. For each that differs, show a
   short diff, then update it.
4. **Never touch:** `inputs/`, `memory/` (user-owned). Never delete user files. If a change
   would require modifying a user-owned file, explain it and ASK — do not auto-apply.
5. Update `./.aleia/version.json` to the new version. Summarize what changed.

## Self-review (report pass/fail with evidence)
- [ ] `inputs/` and `memory/` are byte-for-byte unchanged (verify and cite).
- [ ] Only template-owned files were modified.
- [ ] `./.aleia/version.json` now matches the latest version.
