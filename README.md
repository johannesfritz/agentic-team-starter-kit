# Agentic Team Starter Kit

Materials for the workshop **Agentic AI for Research and Analysis** (19 May 2026), delivered by Dr Johannes Fritz, CEO of the St. Gallen Endowment for Prosperity through Trade and the Digital Policy Alert.

The point of the workshop in one line: *don't write the same prompt twice.*

## What this is

A reproducible starter kit for the live demo. Two Claude Projects + two Skills that together turn a long policy document into a 300-word three-section brief, edited for an expert non-jargon audience.

Free tier of `claude.ai` is all you need.

## The demo, in three panels

Same source document throughout. The output gets sharper as more codification is added.

| Panel | Surface | What you paste | What you attach |
|---|---|---|---|
| 1 — *one-off* | Vanilla `claude.ai` chat, no Project | `01-panel-1-vanilla-chat-prompt.md` (full body) | the source PDF (see below) |
| 2 — *reusable* | A *Policy Brief Drafter* Project you build | Paragraph 1 only of file 01 | the source PDF |
| 3 — *clarified* | A *Clarity Editor* Project you build | Paragraph 2 only of file 01 + Panel 2's output | none |

Panels 2 and 3 together produce a sharper version of the same end-product Panel 1 attempts in one shot.

## Setup order (~30 minutes)

| # | File | Where it goes |
|---|---|---|
| 1 | `04-drafter-project-skill-creator-prompt.md` | Claude Skill Creator → builds Skill 1: *Three-Section Policy Brief Format* |
| 2 | `07-editor-project-skill-creator-prompt.md` | Claude Skill Creator → builds Skill 2: *Clarity Edit Procedure* |
| 3 | `02-drafter-project-system-prompt.md` | New Project "Policy Brief Drafter" → custom instructions |
| 4 | `03-drafter-project-knowledge.md` | Same Project → Project knowledge tab |
| 5 | Skill 1 | Same Project → attach the Skill |
| 6 | `05-editor-project-system-prompt.md` | New Project "Clarity Editor" → custom instructions |
| 7 | `06-editor-project-knowledge.md` | Same Project → Project knowledge tab |
| 8 | Skill 2 | Same Project → attach the Skill |

## The three rungs of customisation

When you click into either Project's settings on `claude.ai`, you see three pieces of codification — each one named on the workshop's *Information and Capability* slide:

1. **System prompt** — the agent's brief.
2. **Project Knowledge file** — the agent's standing reference (the "data file" rung of the Information axis).
3. **Attached Skill** — a reusable procedure (the "skill" rung of the Capability axis).

The PDF you paste is *today's input*. The Project Knowledge file is what the agent always has on its desk. Keeping these separate is the teaching point.

## Source document

The demo uses *Why digital is different* — the SGEPT / Hinrich Foundation report on twenty-first-century digital trade policy. Please download it directly from the Hinrich Foundation:

**[hinrichfoundation.com/research/wp/tech-digital-trade/why-digital-is-different](https://www.hinrichfoundation.com/research/wp/tech-digital-trade/why-digital-is-different)**

Save the PDF locally; you will attach it in Panels 1 and 2.

If you adapt this kit for your own audience, please point them to the Hinrich Foundation as well rather than redistributing the PDF — a small courtesy that keeps the publishing relationship healthy.

## Homework — by Friday

Build the Drafter Project for one of *your* recurring research tasks. Free tier works.

Email a screenshot of the first useful output to johannes.fritz@sgept.org. The first 25 emails get a personal reply with one specific way to make your Drafter sharper.

## Geographic fallback

If `claude.ai` is not available in your region, the same instructions work in ChatGPT Custom GPTs (paid) or Google AI Studio (free, system-instructions only). The abstraction is portable.

## License

MIT. Adapt and reuse however you like. Credit appreciated if you do.
