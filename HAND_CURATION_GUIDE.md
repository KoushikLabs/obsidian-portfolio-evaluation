---
type: guide
title: "Hand-Curation Guide"
updated: 2026-06-19
---

# Hand-Curation Guide

How to maintain this vault by hand. There is **no automated pipeline** — you (or
Claude, on request) edit notes directly. Keep it consistent with [[CLAUDE|the
schema]].

## Obsidian basics

- Open `H:\Obsidian\Portfolio Evaluation` as a vault in Obsidian.
- Start from [[index|the index]]. Use the graph view to see how notes connect, and
  the tag pane to browse by topic.
- Links are **path-based aliased wikilinks**: type `[[` then the folder/slug, then
  `|` and the text you want shown.

## Adding a new note

1. **Pick the type:** concept, method, case-study, entity (org/person), source
   (external-source summary), or template.
2. **Create the file** in the matching folder with a **lowercase-kebab** name
   (case-studies keep their `{CODE}-{slug}` form).
3. **Copy the frontmatter block** for that type from [[CLAUDE|CLAUDE.md]] and fill
   it in. `title` is double-quoted Title Case; `tags` lead with the type echo.
4. **Write the body.** For evaluative content: contribution not attribution, show
   confidence, surface gaps. Preserve `*(stub)*` status honestly — don't fabricate.
5. **Wire it in:** add it to the relevant `{folder}-index.md` table and to
   [[index|index.md]] (bump the counts line), and link it from related notes.

## The `## Notes` convention

Anything under a trailing `## Notes` heading is **hand-editable and durable**. Put
your own synthesis, tensions, and open questions there. (If the vault is ever put
under an automated rebuild, content above `## Notes` may be regenerated; content
from `## Notes` down is preserved verbatim.)

## Updating index & overview counts

When you add or remove notes, update:
- the counts line at the top of [[index|index.md]],
- the relevant table in `index.md`,
- the narrative in [[overview|overview.md]] if a theme changes,
- add a dated entry to the top of [[log|log.md]].

## Link hygiene

- Always path-based aliased wikilinks; **escape `\|`** inside table cells.
- Heading links use the **literal heading text**, not a slug.
- External URLs stay as markdown `[text](https://…)`.
- Run Obsidian's *unresolved links* check after a batch of edits.

## Source-handling

Never import, link, or feed the private conference slides
(`Conference-2026-slides-for-sharing/`) into the vault or NotebookLM. Only the
public Norad PDF is stored (under `attachments/`). See [[CLAUDE|the schema]].
