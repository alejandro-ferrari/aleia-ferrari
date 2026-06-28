# Aleia Ferrari for Claude Cowork — setup

**Step 1 (you):** In Claude Cowork → New Project → "Comenzar desde cero" (create a new
folder, any name) → create the project.

**Step 2 (you):** Paste the block below into that project's chat.

```text
You are setting up "Aleia Ferrari for Claude Cowork" in THIS project's connected folder.
Reply to the user in their language. Do the following, reporting each step:

1. Clone the source:
   git clone --depth 1 https://github.com/alejandro-ferrari/aleia-ferrari /tmp/aleia-src

2. Copy the CONTENTS of /tmp/aleia-src/template/ into the ROOT of this project's connected
   folder, preserving structure (CLAUDE.md, .claude/skills/, inputs/, memory/, briefs/,
   outputs/). IMPORTANT: do NOT overwrite any existing file under inputs/ or memory/ that
   already contains the user's own content.

3. Verify CLAUDE.md and .claude/skills/ now exist in the project folder; list them.

4. Read and FOLLOW .claude/skills/aleia-onboard/SKILL.md to onboard the user right now
   (short questionnaire → memory/people.md).

5. After onboarding, offer to generate their first brief by following
   .claude/skills/brief/SKILL.md.

6. Finally tell the user, in BOTH English and their own language:
   - "To use this later, just ask in natural language — e.g. 'give me today's brief'. There
     are no slash commands."
   - "For best results, fully quit Claude (Cmd+Q) once and relaunch so this project is
     freshly indexed."

Only modify files inside this project folder.
```
