# Skill 2 — Clarity Edit Procedure

This file gives you everything you need to create the second Skill on `claude.ai`.

## Quick reference

| Field | Value |
|---|---|
| **Name** | `Clarity Edit Procedure` |
| **Description** | `Edit a draft policy brief for an expert non-jargon audience; return the edited text only.` |
| **Instructions** | See "Instructions body" below — paste everything below the `---` line |
| **Reference file** *(if Skill Creator accepts attachments)* | `06-editor-project-knowledge.md` |
| **Attach to (after creation)** | The **Clarity Editor** Project |

## How to create it on `claude.ai`

1. Click your profile (bottom-left) → **Settings** → **Capabilities** → **Skills** → **Create skill**. (If the Skills menu lives somewhere else in your account, look under *Capabilities* or as a top-level sidebar entry.)
2. The Skill Creator opens in one of two modes:
   - **Form mode:** fields for Name, Description, Instructions. Fill them in directly from the table above.
   - **Chat mode:** Claude asks you to describe what the Skill should do. Paste the body below the `---` line at the bottom of this file. Claude generates the Skill for you.
3. If a *Reference file* field appears, attach `06-editor-project-knowledge.md`. If not, skip — the same file goes into the Editor Project's knowledge tab in the next setup step.
4. Click **Create**.

## Attach it to the Project

Open the **Clarity Editor** Project → settings → **Skills** (or **Capabilities**) → toggle *Clarity Edit Procedure* on. Save.

---

## Instructions body — paste below this line into the Skill Creator

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
