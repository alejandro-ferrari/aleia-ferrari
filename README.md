# Aleia Ferrari for Claude Cowork

A productivity starter for Claude Cowork. It installs a spec-first, evidence-reviewed working
method (the LonelyOctopus method improved with Karpathy's spec-first approach) into a Cowork
project — operating instructions, a guided onboarding, a daily brief, and project planning.

**Distribution:** not a marketplace plugin (Cowork doesn't support third-party plugin install
for non-technical users yet). Instead, Cowork sets itself up from a master prompt that clones
this repo into your project folder. Skills live in the project's `.claude/skills/` and are
invoked in natural language — no slash commands.

## Install (≈2 minutes)

1. Claude Cowork → **New Project → "start from scratch"** → create a new folder.
2. Paste the master prompt from [`setup-prompt.md`](./setup-prompt.md) into the project chat.
3. Answer the short onboarding questions; get your first brief.
4. Fully quit + relaunch Claude once so the project is freshly indexed.

Then just ask in natural language: *"give me today's brief"*, *"help me plan X"*.

## What gets installed (`template/`)
- `CLAUDE.md` — operating instructions + skill routing (auto-loaded by Cowork).
- `.claude/skills/` — `aleia-onboard`, `brief`, `plan`.
- `inputs/` (your inbox — never auto-overwritten), `memory/` (your profile), `briefs/`, `outputs/`.

> Status: v0.0.1 — early build. Roadmap toward v1.0.0 in the product PRD.
