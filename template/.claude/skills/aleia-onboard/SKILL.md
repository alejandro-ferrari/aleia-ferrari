---
name: aleia-onboard
description: First-run onboarding for Aleia Ferrari for Claude Cowork. Builds a user-confirmed profile via a short questionnaire and writes it to memory/people.md. Trigger on first run or when the user asks to set up / re-onboard.
---

# Onboarding — build the user profile

Goal: a user-confirmed profile that personalizes everything, with minimal effort and full
privacy. Interact in the user's language (ask which language first if unknown).

## Steps

1. Greet briefly. Explain this takes ~2 minutes and they can skip any question.
2. Ask the following, ONE or TWO at a time, each with a few suggested options AND the option
   to free-type. Keep it light:
   - Name; what they do (role / work / projects).
   - Which AI they currently use (Claude / ChatGPT / other).
   - Top 2–3 recurring tasks or pain points they want help with.
   - What a useful "daily brief" would include for them.
   - Timezone; preferred language.
3. **Privacy:** do NOT ask for sensitive data (health, finances, credentials, third-party
   private info). If the user volunteers something sensitive, do not store it.
4. Show the assembled profile back **field by field** and ask them to confirm / edit / delete.
   Call it a "user-confirmed profile", never "verified".
5. On confirmation, write it to `memory/people.md` (user-owned). If the file already has
   content, show a diff and confirm before changing.
6. Offer to generate their first brief now (follow `.claude/skills/brief/SKILL.md`).

## Self-review before finishing (report pass/fail with evidence)

- [ ] `memory/people.md` exists and contains the confirmed fields.
- [ ] Nothing the user asked to remove was stored.
- [ ] Nothing sensitive was stored.
