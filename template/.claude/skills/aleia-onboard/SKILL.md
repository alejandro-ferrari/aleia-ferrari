---
name: aleia-onboard
description: First-run onboarding for Aleia Ferrari for Claude Cowork. Builds a user-confirmed profile (about-me + working style + domains) and writes it to memory/people.md. Trigger on first run or when the user asks to set up / re-onboard.
---

# Onboarding — build the user's profile (propose, don't interrogate)

Purpose: capture exactly what the method needs to personalize itself, with minimal friction
and full privacy. Everything you ask must feed one of three things:
(1) how to behave as their partner, (2) what to build for them, (3) what a useful brief looks like.

Interact in the user's language (ask once if unknown). Keep it to ~2–3 minutes.

## Phase 0 — Orient first
Before asking anything, use any context already available (this conversation, files already in
the project). Pre-fill every field you can infer, and show it as "here's what I think — correct
anything", so the user only fixes/fills gaps. Never ask what you can already answer.

## Offer two tracks (let the user choose)
- **Quick (default):** the short questionnaire below.
- **Deep (optional):** tell them they can let their existing AI pre-fill the profile — point
  them to `context-extraction-prompt.md` in this project's folder (they paste it into their
  ChatGPT/Claude, review the output, paste it back). Then reconcile it field by field.

## The questionnaire — ask 1–2 at a time, each with suggested options + free-type
Group A — About you: name; what you do (role / work / main projects); tools + which AI you use.
Group B — Working style (this calibrates how I behave): how direct vs detailed you want me;
how much push-back you want; anything I must NEVER do automatically.
Group C — Goals/pains: your top 2–3 recurring tasks or headaches you want help with.
Group D — Brief shape: what a useful daily brief would include for you; timezone; language.

## Propose, don't interrogate — domains
From A–C, PROPOSE 3–5 candidate domains/workflows this system could cover (one line each, why
it fits), as a pick-list. The user picks the ones they want and can add one. Don't ask
open-ended "what do you want to build".

## Privacy (hard rules)
Never ask for or store: health, finances, legal matters, credentials, home address, or private
info about third parties. If volunteered, don't store it. If using the Deep track, remind the
user to strip anything sensitive before pasting.

## Confirm + write
Show the assembled profile **field by field**; the user confirms / edits / deletes. It is a
"user-confirmed profile", never "verified". On confirmation, write `memory/people.md`
(user-owned) — if it already has content, show a diff first. Record the chosen domains there too.

## Self-review before finishing (report pass/fail with evidence)
- [ ] `memory/people.md` exists and contains the confirmed fields + chosen domains.
- [ ] Nothing the user removed, and nothing sensitive, was stored.
- [ ] Every stored item came from the user (or was confirmed) — no invented facts.

Then offer to generate their first brief (`.claude/skills/brief/SKILL.md`).
