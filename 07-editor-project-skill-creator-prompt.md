# Skill Creator — Clarity Edit Procedure

**What to do**
1. On `claude.ai`, open the Skill Creator (Settings → Skills → Create skill).
2. Paste the body below as the description / instructions input.
3. If the Skill Creator UI accepts attachments, attach `06-editor-project-knowledge.md` as the reference file. If not, the same file lives in the Clarity Editor Project's Knowledge tab and the Skill will reference it from there.
4. Once created, attach the resulting Skill to the **Clarity Editor** Project.

---

Create a Skill called "Clarity Edit Procedure".

Purpose: take a draft policy brief and edit it for an expert, non-jargon audience. Return the edited brief only — never a critique, never a diff, never a change list.

When the user pastes a draft brief, the Skill should:

- Preserve every factual claim in the input. Do not add new claims.
- Preserve the three-section structure (What happened / Why it matters / What to watch next).
- Stay under 300 words total.
- Apply the bracket method: remove every word not doing necessary work.
- Swap pomposity for plain words ("utilize" → "use", "facilitate" → "help", "in order to" → "to").
- Replace trade-policy jargon with plain language. If a technical term cannot be avoided, define it inline in five words or fewer.
- Prefer active voice. One idea per sentence.

Output is the final edited brief only. No prefix, no suffix, no commentary.

The Skill should reference the attached "Clarity Editing for Expert, Non-Jargon Audiences" document for bracket targets, clutter swaps, and forbidden vocabulary.
