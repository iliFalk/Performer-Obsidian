# Performer — reference

The README covers the start. This file keeps the templates, the capabilities and the build.

## Templates

A template is a name plus three prompts: how the note is named, what each property must hold, and
what the body should become.

### Example: a project brief

- **Note name:** "Create a formal project ID: [PROJECT-CODE] [Subject]"
- **Frontmatter:** `priority` — "High, Medium, or Low based on urgency"; `stakeholders` —
  "List all departments involved"; `deadline` — "Extract the final delivery date"
- **Body:** "Summarize into Objectives, Risks, and Next Steps"

### Example: a trip planner

- **Note name:** "Suggest a title like '2025 - [City] Trip Planning'"
- **Frontmatter:** `destination` — "Extract the city and country"; `budget` — "Estimate the total
  cost mentioned"; `days` — "Count how many days the trip lasts"
- **Body:** "Format as a bulleted itinerary with sections for 'Must-See' and 'Food'"

## Capabilities

- **The loupe** — the overlay slides over the note instead of opening a separate window.
- **Metadata synthesis** — titles, authors, dates and types are extracted into frontmatter, so the
  vault becomes a queryable database.
- **Deep restructuring** — the body is rewritten into a consistent shape for long-term storage.

## The idea

The plugin is a magnifier for a personal knowledge base: it does not add new content, it makes the
structure that is already in the note visible.

## Build

```bash
npm install
npm run build     # esbuild, writes main.js next to manifest.json
```

Copy `main.js`, `manifest.json` and `styles.css` into `<vault>/.obsidian/plugins/performer/` for a
manual install.

## Stack

React 19 and Vite for the overlay, Motion for the transitions, OpenRouter for the model.
