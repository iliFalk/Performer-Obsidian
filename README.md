# Performer

Obsidian plugin that interprets a note with AI and rewrites its structure.

![The Performer overlay working on a note](./assets/performer-workflow-banner.png)

- **What it is:** an Obsidian plugin in TypeScript, built with esbuild, that calls OpenRouter.
- **What it does:** reads a note and rewrites it — frontmatter properties filled in, body restructured by a template you choose — so a rough draft becomes a record you can search later.
- **What it needs:** Obsidian 1.4 or newer, the BRAT plugin to install it, and an OpenRouter key.
- **How do I start:** install BRAT, then add `https://github.com/iliFalk/Performer-Obsidian` as a beta plugin; enable Performer and paste your key.

## Install

1. Install **BRAT** from Obsidian's community plugins.
2. In BRAT settings press **Add beta plugin** and paste `https://github.com/iliFalk/Performer-Obsidian`.
3. Enable **Performer** in the community plugin list.
4. Open Performer's settings and paste your OpenRouter key.

## Use

1. Open any note and press the **Performer** ribbon icon, or run the command from the palette.
2. Pick a template — Meeting, Book, or one you wrote yourself — and press **PERFORM**.
3. Check the properties and the restructured body, change what is wrong, then press **Update Note**.

Before and after, on the same three lines:

```markdown
meeting with Sarah today about the solar project.
we talked about the panels and the deadline is next friday.
sarah says we need more cables.
```

```markdown
---
title: Solar Project - Panel Logistics & Deadlines
participants: Sarah
type: meeting
---

## Discussion
- Review of current panel status.
- Deadline confirmed for next Friday.

## Action Items
- [ ] Order additional cables (Requested by Sarah).
```

## Settings

| Setting | Meaning |
|---|---|
| OpenRouter key | the key every run is billed to; it stays in the plugin's data file |
| Model | which model performs the note — Gemini, GPT or Claude |
| Templates | the prompts behind each performance: note name, frontmatter fields, body shape |

A template is three prompts: one names the note, one fills each property, one shapes the body.

## Docs

- `docs/DEVELOPMENT.md` — templates in full, the capabilities, the stack, and how to build the plugin.
- `LICENSE` — MIT.
