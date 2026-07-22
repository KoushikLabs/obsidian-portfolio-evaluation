# Portfolio Evaluation Wiki — Schema (single-domain, hand-authored)

This vault is a hand-authored knowledge base on **portfolio-level evaluation**
for funders and incubators. Unlike the multi-creator sibling vaults (Skool
Resources etc.), it has **no scraper / NotebookLM-ingest / Readwise pipeline** —
it is curated by hand. A companion NotebookLM notebook is built *from* these
notes (see [[CLAUDE#NotebookLM]]).

## Layout

```
concepts/         foundational ideas (what a portfolio is, heterogeneity, …)
methods/          the building-block methods (Outcome Harvesting, rubrics, …)
case-studies/     structured write-ups of real portfolio evaluations
orgs-and-people/  the orgs/specialists who do this work (type: entity)
external-sources/ structured summaries of foundational published guidance (type: source)
templates/        reusable artefacts + reusable Claude prompts (prompts.md)
attachments/      binary attachments (the Norad PDF)
index.md          master MOC — read first
overview.md       narrative synthesis (has a hand-editable ## Notes section)
log.md            append-only changelog (newest at top)
CLAUDE.md         this schema / operating contract
HAND_CURATION_GUIDE.md   how to maintain the vault by hand
OPERATING_MANUAL.md      short runbook
{folder}-index.md        per-folder index note (was README.md)
```

## Frontmatter conventions

Every note has YAML frontmatter. Fields are unquoted **except** `title` (always
double-quoted) and `published`/`template_version` (quoted). Dates are ISO
`YYYY-MM-DD`. `tags` and `sources` are inline flow lists.

```yaml
# concept / method
type: concept            # or: method
title: "Display Title"
tags: [concept, topic-a, topic-b]      # first token echoes `type`
created: 2026-06-19
updated: 2026-06-19
source_count: 0                         # number of external-source notes cited
sources: []                             # their basenames, e.g. [norad-portfolio-mel-guide-summary]

# case-study
type: case-study
title: "Session Title (without the code prefix)"
tags: [case-study, conference-ukes-2026, topic]
created: 2026-06-19
updated: 2026-06-19
session_id: T0302                       # conference code
presenter: Niki Wood                    # omit if "(not confirmed from programme)"
org: integrity-global                   # entity slug; omit if unknown
conference: UK Evaluation Society 2026
source_count: 0
sources: []

# entity (orgs & people)
type: entity
title: "Itad"
tags: [entity, org, topic, slug]
created: 2026-06-19
updated: 2026-06-19
source_count: 2
sources: [norad-portfolio-mel-guide-summary, itad-portfolio-mel-brief-summary]

# source (external-source summary)
type: source
title: "Norad — A Practical Guide to MEL at a Portfolio Level"
tags: [source, guidance, topic]
created: 2026-06-19
updated: 2026-06-19
publisher: Norad (...)
published: "2024-09"
authors: Rob Lloyd & Catrin Hepworth (Itad)
url: https://...
source_count: 1
sources: []

# template
type: template
title: "..."
tags: [template, topic]
created: 2026-06-19
updated: 2026-06-19
template_version: "1.0"                 # omit for prompts.md

# index / overview / log / guide / manual
type: index | overview | log | guide | manual
title: "..."
updated: 2026-06-19                      # index uses updated only
```

## Wikilink style

**Path-based, aliased wikilinks** everywhere: `[[folder/slug|Display Text]]`
(no `.md`, full vault-relative path). This is collision-proof — important because
several notes share short names and the source had seven `README.md` files.

- Inside **table cells**, escape the alias pipe: `[[case-studies/T0302-portfoli-omg\|T0302]]`.
- **Heading links** use the *literal* heading text: `[[external-sources/norad-portfolio-mel-guide-summary#5. The five-step model (the spine of the guide)|…]]` — not the GitHub-slug.
- **External URLs** stay as markdown links `[text](https://…)`. Do not wikilink them.
- The PDF attachment is a **non-embed** wikilink `[[attachments/norad-portfolio-mel-guide-2024.pdf]]` (no `![[…]]`).
- No block links `[[#^…]]`, no embeds `![[…]]`.

## Note naming

Lowercase kebab-case filenames; the Title Case label lives in `title:` and in
link aliases. Case-study files keep their `{CODE}-{slug}.md` form (the conference
session code is the stable ID — a deliberate deviation from the siblings'
`{date}-{slug}` source naming). Folder index notes are `{folder}-index.md`.
Runbooks are `SCREAMING_SNAKE_CASE`; generated MOCs are lowercase.

## Tag taxonomy

Flat, lowercase, kebab-case tokens, declared only in frontmatter (no inline
`#hashtags`, no nested `#a/b`). The **first** tag echoes the note `type`; the rest
are topical, drawn from the controlled vocabulary: `portfolio-evaluation,
portfolio-mel, heterogeneity, aggregation, attribution, contribution,
theory-of-change, oecd-dac, criteria, rubrics, outcome-harvesting,
contribution-analysis, appreciative-inquiry, evidence-gap-maps,
value-for-investment, cross-case-analysis, evidence-synthesis, credibility,
evidence-quality, funders, incubators, evaluation-culture, learning-systems,
standing-function, dashboards, communication, funder-brief, actionability, ai,
ai-in-evaluation, conference-ukes-2026`, plus per-entity slug tags.

## Workflows (hand-curation; no automated pipeline)

**Add a new note:** pick the type → create a kebab-case file in the right folder →
copy the matching frontmatter block above → write the body → add it to the
relevant `{folder}-index.md` and to `index.md` (update counts) → link it from
related notes with path-aliased wikilinks.

**Update the index:** when notes are added/removed, refresh the counts line and
the relevant table in `index.md`, and the narrative in `overview.md`.

**Answer a query:** read `index.md` to find candidate pages → read the
concept/method/case-study/source notes → synthesise with path-aliased wikilinks to
cited pages. Contribution not attribution; show confidence; surface gaps.

## Hand-curation & Notes preservation

A trailing `## Notes` section (marked *"Hand-editable. Preserved across any future
rebuild."*) holds hand-written synthesis. If this vault is ever put under an
automated rebuild, everything from `## Notes` down must be kept verbatim;
everything above may be regenerated. Today there is no rebuild script, so this is
forward-looking — but keep durable hand-synthesis under `## Notes`.

## Source-handling (non-negotiable)

- The **conference slides** (`Conference-2026-slides-for-sharing/`, kept *outside*
  this vault) are **private, personal-reference-only — never redistribute, quote
  publicly, or feed into NotebookLM or any external tool.**
- The Norad PDF (public) is the only stored attachment.
- Case-study notes are written from the *public* conference programme, not the slides.

## NotebookLM

A companion NotebookLM notebook is built from this vault's text notes (concepts,
methods, case-studies, orgs, external-source summaries, templates) plus the public
Norad PDF — for AI Q&A/synthesis. The private slides are excluded.

- **Notebook URL:** https://notebooklm.google.com/notebook/31783208-b578-4b1e-a7b3-4dd83757d501 (title: *Eval - Portfolio Evaluation*)
- **Sources (9):** 4 primary documents as URLs (Norad PDF, Itad article, Abt PMEL Nepal project page, Abt PMEL blog) + 5 curated text bundles (overview & source summaries; concepts; methods; case studies; orgs/templates/learning).
- **Known gap:** the Sarah Dickins Medium article could not be added as a URL source (Medium blocks server-side fetchers) — add it manually if wanted; its content is described in the curated bundle.
