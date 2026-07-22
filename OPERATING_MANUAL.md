---
type: manual
title: "Operating Manual"
updated: 2026-06-19
---

# Operating Manual

A short runbook for this vault. It is a **hand-curated** knowledge base — there is
no scraper, Readwise, Kortex, or scheduled task (by design; scope was
structure + content + a NotebookLM notebook).

## What this vault is

A reference + self-study base on portfolio-level evaluation for funders and
incubators. Front door: [[index|index.md]]. Learning route:
[[learning-plan|Learning Plan]].

## Routine tasks

| When | Do |
|---|---|
| Whenever you learn something worth keeping | Add/extend a note (see [[HAND_CURATION_GUIDE|Hand-Curation Guide]]); log it in [[log|log.md]]. |
| After adding/removing notes | Update counts + tables in [[index|index.md]]; refresh [[overview|overview.md]] if a theme shifts. |
| Periodically | Run Obsidian's *unresolved links* check; skim the tag pane for stray/duplicate tags. |
| When new sources surface | Add a `type: source` summary in `external-sources/`; optionally add it to the NotebookLM notebook. |

## NotebookLM companion

A NotebookLM notebook is built from this vault's text notes + the public Norad
PDF, for AI Q&A. Its URL is recorded in [[CLAUDE#NotebookLM|CLAUDE.md]] and
[[log|log.md]]. To refresh it after major additions, re-add the changed notes as
sources. **Never** add the private conference slides.

## Optional future upgrades (not set up)

If this ever needs to become a live, compounding pipeline (scrapers, Readwise
newsletter ingest, weekly auto-rebuild) like the Skool Resources vault, that
machinery can be added later — see the `knowledge-base-pipeline` skill. It is
intentionally **not** installed here.
