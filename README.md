# Agentic Team Starter Kit

**Build a two-agent team that turns a long policy document into a 300-word brief, edited for an expert non-jargon audience.**

From the workshop *Agentic AI for Research and Analysis* (19 May 2026), Dr Johannes Fritz, SGEPT / Digital Policy Alert.

You can follow along live during the workshop, or reproduce the whole demo afterwards in about 30 minutes. Free tier of `claude.ai` is all you need.

> **The point in one line:** *Don't write the same prompt twice.*

---

## Before you start (5 minutes)

You need three things ready:

1. **A free Claude account.** Sign up at [claude.ai](https://claude.ai). The whole demo runs on the free tier.
2. **The source document.** Download *Why digital is different* from the Hinrich Foundation: [hinrichfoundation.com/research/wp/tech-digital-trade/why-digital-is-different](https://www.hinrichfoundation.com/research/wp/tech-digital-trade/why-digital-is-different). Save the PDF locally — you will attach it in Panels 1 and 2.
3. **This repo open in a browser tab.** You will copy text from these files into Claude.

If `claude.ai` is unavailable in your region, see **Fallbacks** at the bottom.

---

## What you are going to build

Two **Projects** — each one a specialised agent on `claude.ai`. Each Project carries three pieces of customisation:

| Rung | What it is | Where it lives in `claude.ai` |
|---|---|---|
| **System prompt** | The agent's job description (its brief) | Project → *Custom instructions* |
| **Project Knowledge** | The agent's standing reference document | Project → *Project knowledge* |
| **Skill** | A reusable procedure the agent follows | Created once, attached to any Project |

Your two Projects:

- **Policy Brief Drafter** — reads a source document, produces a structured 300-word brief.
- **Clarity Editor** — takes that draft and rewrites it for an expert non-jargon audience.

The PDF you paste in is *today's input*. It is not Project Knowledge — keep these separate in your head. That distinction is the main teaching point of the workshop.

---

## Part A — Build your team (~20 minutes, one-time setup)

Do this **before** the live demo if you can. The Drafter and Editor each take ~10 minutes to wire up.

### Step 1 — Create Skill 1: *Three-Section Policy Brief Format*

1. On `claude.ai`, click your profile (bottom-left of the sidebar) → **Settings** → **Capabilities** → **Skills** → **Create skill**.
2. Open [`04-drafter-project-skill-creator-prompt.md`](04-drafter-project-skill-creator-prompt.md) in this repo. Copy everything below the `---` line and paste it into the Skill Creator.
3. *(Optional)* If the Skill Creator UI lets you attach a reference file, attach [`03-drafter-project-knowledge.md`](03-drafter-project-knowledge.md). If not, no problem — that file goes into the Project itself in Step 3.
4. Click **Create**. Note the Skill name.

### Step 2 — Create Skill 2: *Clarity Edit Procedure*

Same as Step 1, but with:
- The prompt body from [`07-editor-project-skill-creator-prompt.md`](07-editor-project-skill-creator-prompt.md).
- *(Optional)* reference attachment [`06-editor-project-knowledge.md`](06-editor-project-knowledge.md).

### Step 3 — Build the Policy Brief Drafter Project

1. On `claude.ai`, click **Projects** in the sidebar → **New project**. Name it **Policy Brief Drafter**.
2. **Custom instructions:** open [`02-drafter-project-system-prompt.md`](02-drafter-project-system-prompt.md). Copy everything below the `---` line. Paste into the *Custom instructions* field.
3. **Project knowledge:** upload [`03-drafter-project-knowledge.md`](03-drafter-project-knowledge.md) to the *Project knowledge* tab.
4. **Skills:** attach Skill 1 (*Three-Section Policy Brief Format*) from Step 1.
5. Save.

### Step 4 — Build the Clarity Editor Project

1. **New project**, name it **Clarity Editor**.
2. **Custom instructions:** body of [`05-editor-project-system-prompt.md`](05-editor-project-system-prompt.md).
3. **Project knowledge:** upload [`06-editor-project-knowledge.md`](06-editor-project-knowledge.md).
4. **Skills:** attach Skill 2 (*Clarity Edit Procedure*).
5. Save.

> ✅ **You now have a two-agent team.** Each agent has a brief, a reference, and a procedure. The same scaffold works for any recurring research task.

---

## Part B — Run the demo (~10 minutes)

You will run the same task three ways. The output gets sharper as you add more codification.

### Panel 1 — One-off (vanilla chat)

1. Open a **new chat** on `claude.ai`. Do **not** select a Project.
2. **Attach** the Hinrich PDF you downloaded.
3. Open [`01-panel-1-vanilla-chat-prompt.md`](01-panel-1-vanilla-chat-prompt.md). Copy **everything below the `---` line** (both paragraphs). Paste into the message box. Send.

Read the output. One agent did two jobs (draft + self-edit) in one turn. Note where it feels uneven.

### Panel 2 — Reusable (the Drafter Project)

1. Open your **Policy Brief Drafter** Project.
2. Click into the Project's settings briefly to confirm three pieces of codification are visible: *Custom instructions* (system prompt), *Project knowledge* (the SGEPT style file), and an attached *Skill*. This is what makes the Drafter the Drafter.
3. Start a new chat inside the Project.
4. **Attach** the Hinrich PDF.
5. From [`01-panel-1-vanilla-chat-prompt.md`](01-panel-1-vanilla-chat-prompt.md), copy **only the first paragraph** — the one beginning *"First, draft a 300-word policy brief..."*. Delete the word **"First, "** at the start so the prompt begins *"Draft a 300-word..."*. Paste. Send.

Notice the BLUF voice, the three labelled sections, and the citations to the source. The format is consistent because the Skill enforces it.

### Panel 3 — Clarified (the Clarity Editor Project)

1. **Copy Panel 2's output** to your clipboard.
2. Open your **Clarity Editor** Project. Start a new chat inside it. (No PDF attached this time — the Editor only sees the draft.)
3. From [`01-panel-1-vanilla-chat-prompt.md`](01-panel-1-vanilla-chat-prompt.md), copy **only the second paragraph** — the one beginning *"Then, edit your draft..."*. Replace **"Then, edit your draft"** with **"Edit the brief below"**. On a new line, type `---`. Below the `---`, paste Panel 2's output.
4. Send.

You now have the final-final output: a brief that is **both** structured (the Drafter's gift) **and** plain-language (the Editor's gift). Place Panel 1's final paragraph next to Panel 3's final paragraph and read them aloud. They sound different.

---

## What just happened

You built three rungs of customisation, all named in the workshop's *Information and Capability* slide:

1. **The system prompt** is the agent's brief — the *Composition* pillar.
2. **The Project Knowledge file** is a *data file* on the Information axis — what the agent always has on its desk.
3. **The Skill** is the agent's *procedure* on the Capability axis — a recipe you wrote once and can attach to any future Project.

Two specialised agents (Drafter + Editor) produced a noticeably better final brief than one generalist agent doing both jobs at once (Panel 1). The agents shared nothing but the copy-paste you did between them. **You were the orchestrator.** In a fuller agentic system, an orchestrator agent would do that copy-paste automatically — but the substance is exactly the same.

That is *agentic work* at its entry level.

---

## Homework — by Friday

Build a *Drafter Project* for one of **your own** recurring research tasks. The scaffold transfers directly:

- **System prompt** = your job description for the agent.
- **Project knowledge** = your house style guide, glossary, or reference doc.
- **Skill** = your output format.

Email a screenshot of the first useful output to **johannes.fritz@sgept.org**. The first 25 emails get a personal reply with one specific way to make your Drafter sharper.

---

## Troubleshooting and fallbacks

- **Skills option not visible in your account.** Skills are rolling out gradually. If you do not see the Skills menu, paste the Skill body directly into the Project's system prompt below the existing instructions. The output is slightly less elegant but the demo still works.
- **Your output is different from the speaker's.** Normal. Output varies by model version, by token sampling, and by exactly how you paste. The teaching point is the *gradient* across the three panels, not the specific wording.
- **The Drafter cites things that aren't in the PDF.** Re-read the system prompt — the grounding rule should suppress that. If the Drafter still hallucinates, edit the prompt to be more explicit (for example: *"If the source does not say it, omit it. Do not infer."*). **Iteration on the prompt is the work.**
- **`claude.ai` is blocked in your region.** The same scaffold works in **ChatGPT Custom GPTs** (paid) or **Google AI Studio** (free, system-instructions only). Paste each Project's system prompt into the system-instructions field; upload the knowledge file as a reference; use the same user prompts in Panels 1, 2, 3.
- **Skill Creator does not accept a reference file.** Skip the attachment step. The same reference file is already uploaded to the Project's *Project knowledge* tab — the Skill will reference it from there.

---

## File map

| File | What it is | Where it goes |
|---|---|---|
| `README.md` | This file — read first | — |
| `01-panel-1-vanilla-chat-prompt.md` | The user prompt for Panel 1 (both paragraphs) | Pasted into vanilla chat (Panel 1); paragraph 1 into Drafter (Panel 2); paragraph 2 into Editor (Panel 3) |
| `02-drafter-project-system-prompt.md` | Drafter Project custom instructions | Paste into the Drafter Project |
| `03-drafter-project-knowledge.md` | SGEPT briefing voice essentials | Upload to Drafter Project knowledge |
| `04-drafter-project-skill-creator-prompt.md` | Prompt to build Skill 1 | Paste into Skill Creator |
| `05-editor-project-system-prompt.md` | Editor Project custom instructions | Paste into the Editor Project |
| `06-editor-project-knowledge.md` | Clarity editing rules (Zinsser bracket method) | Upload to Editor Project knowledge |
| `07-editor-project-skill-creator-prompt.md` | Prompt to build Skill 2 | Paste into Skill Creator |
| `LICENSE` | MIT | — |

---

## Source document — courtesy note

The demo uses *Why digital is different* by the Hinrich Foundation and SGEPT. Please download it directly from the Hinrich Foundation: [hinrichfoundation.com/research/wp/tech-digital-trade/why-digital-is-different](https://www.hinrichfoundation.com/research/wp/tech-digital-trade/why-digital-is-different).

If you adapt this kit for your own audience, please point them to the Hinrich Foundation rather than redistributing the PDF — a small courtesy that keeps publishing relationships healthy.

---

## License

MIT. Adapt and reuse however you like. If you ship something based on this kit, credit appreciated.
