# Skill Creator — Three-Section Policy Brief Format

**What to do**
1. On `claude.ai`, open the Skill Creator (Settings → Skills → Create skill).
2. Paste the body below as the description / instructions input.
3. If the Skill Creator UI accepts attachments, attach `03-drafter-project-knowledge.md` as the reference file. If not, the same file lives in the Drafter Project's Knowledge tab and the Skill will reference it from there.
4. Once created, attach the resulting Skill to the **Policy Brief Drafter** Project.

---

Create a Skill called "Three-Section Policy Brief Format".

Purpose: enforce the SGEPT in-house format for short policy briefs.

When the user asks for a brief based on a source document, the Skill should produce output that:

- Has exactly three sections labelled "What happened", "Why it matters", "What to watch next".
- Stays under 300 words total.
- Uses bullets where useful, maximum two levels of nesting.
- Grounds every factual claim in a specific passage of the source document. If the source does not say it, the brief does not say it.
- Lists any user-requested claims unsupported by the source under a closing line "Out of scope (not in source)".
- Uses no hedging language. No "perhaps consider", "it could be argued", "some have suggested".

The Skill should reference the attached "SGEPT Briefing Style — Essentials" document for voice and structure rules.

Make the Skill self-contained: do not require the user to repeat the format rules in their prompt.
