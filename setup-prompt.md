# Aleia Ferrari for Claude Cowork — setup prompt (v0.0.1 TEST)

Paste everything inside the code block below into a Claude Cowork chat **inside a project
that points at the (empty) folder where you want your system to live**.

```text
You are setting up "Aleia Ferrari for Claude Cowork" in THIS project's folder (the local
folder this Cowork project is connected to). Do the following in order, using your shell and
file tools, and report the result of each step:

1. Clone the source repo into a temp location:
   git clone --depth 1 https://github.com/alejandro-ferrari/aleia-ferrari /tmp/aleia-src

2. Copy the contents of /tmp/aleia-src/template/ into the ROOT of this project's connected
   folder, preserving structure. This includes: a CLAUDE.md, a .claude/skills/ directory, and
   empty inputs/ , memory/ , briefs/ folders.

3. Verify the project folder now contains: CLAUDE.md, .claude/skills/aleia-hello/SKILL.md,
   and the inputs/ memory/ briefs/ folders. List them to confirm.

4. Tell the user EXACTLY this:
   "✅ Setup complete. Now please CLOSE and REOPEN this Cowork project so it loads the new
   skills, then type /aleia-hello (or run the 'aleia-hello' skill) to confirm it loaded."

Do not do anything else. Do not modify files outside this project folder.
```
