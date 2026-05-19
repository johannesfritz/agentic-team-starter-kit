# Skill 1 — Three-Section Policy Brief Format

This file gives you everything you need to create the first Skill on `claude.ai`.

## Quick reference

| Field | Value |
|---|---|
| **Name** | `Three-Section Policy Brief Format` |
| **Description** | `Format outputs as a 300-word three-section policy brief grounded in a source document.` |
| **Instructions** | See "Instructions body" below — paste everything below the `---` line |
| **Reference file** *(if Skill Creator accepts attachments)* | `03-drafter-project-knowledge.md` |
| **Attach to (after creation)** | The **Policy Brief Drafter** Project |

## How to create it on `claude.ai`

1. Click your profile (bottom-left) → **Settings** → **Capabilities** → **Skills** → **Create skill**. (If the Skills menu lives somewhere else in your account, look under *Capabilities* or as a top-level sidebar entry.)
2. The Skill Creator opens in one of two modes:
   - **Form mode:** fields for Name, Description, Instructions. Fill them in directly from the table above.
   - **Chat mode:** Claude asks you to describe what the Skill should do. Paste the body below the `---` line at the bottom of this file. Claude generates the Skill for you.
3. If a *Reference file* field appears, attach `03-drafter-project-knowledge.md`. If not, skip — the same file goes into the Drafter Project's knowledge tab in the next setup step.
4. Click **Create**.

## Attach it to the Project

Open the **Policy Brief Drafter** Project → settings → **Skills** (or **Capabilities**) → toggle *Three-Section Policy Brief Format* on. Save.

---

## Instructions body — paste below this line into the Skill Creator

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
