# CLAUDE.md

You are the maintainer of this personal wiki.

Your job is to help turn raw material into clean, linked, reusable knowledge.

## Purpose

This vault has two jobs:

1. store raw material
2. grow a long-term wiki from that material

Do not treat the wiki like chat history.
Do not dump random notes into it.
Write pages that stay useful later.

## Vault rules

- `01 - Raw Sources/` holds source material and source captures.
- Raw sources are read-only once saved.
- `02 - Wiki/` holds long-term knowledge pages.
- `03 - Maps/` holds hub pages and route pages.
- `04 - Workbench/` holds scratch work and temporary thinking.
- `05 - Projects/` holds active work, drafts, and delivery notes.
- `06 - Daily/` holds day notes.
- `07 - System/` holds prompts, rules, and templates.
- `90 - Archive/` holds old or inactive material.

## Main writing rules

- Write in plain markdown.
- Prefer short sections and clean bullets.
- Keep one clear topic per page.
- Link to related pages when useful.
- Do not repeat the same knowledge across many pages.
- If a page already exists, update it instead of making a near-duplicate.
- Keep frontmatter and system dates in ISO format: YYYY-MM-DD.
- In normal note text, Swiss-style display dates may use DD-MM-YYYY.
- Put raw facts close to the source they came from.
- Mark unclear points as open questions, not facts.

## Date rules

- Use `YYYY-MM-DD` for frontmatter fields like `created`, `updated`, and `date`.
- Use `YYYY-MM-DD` in logs, file names, and system tracking.
- In normal written text inside notes, Swiss-style dates may use `DD-MM-YYYY`.
- Do not mix date styles inside frontmatter.

## Page priority

When adding new knowledge, pick the right home:

- concept or idea -> `02 - Wiki/Concepts/`
- company or brand -> `02 - Wiki/Companies/`
- person -> `02 - Wiki/People/`
- repeatable way of working -> `02 - Wiki/Processes/`
- reusable project knowledge -> `02 - Wiki/Projects/`
- term or word meaning -> `02 - Wiki/Glossary/`
- hub or topic route page -> `03 - Maps/`

## Raw source policy

- Keep source files unchanged after capture.
- If needed, make a separate source summary page in the wiki.
- A source can update many wiki pages.
- Do not move source text into the wiki in bulk.
- Pull out facts, decisions, ideas, links, open questions, and relations.

## Ingest workflow

When asked to ingest a source:

1. Read the source fully.
2. Identify:
   - main topic
   - facts
   - decisions
   - people
   - companies
   - processes
   - projects
   - open questions
3. Check whether matching wiki pages already exist.
4. Update existing pages first.
5. Create new pages only when needed.
6. Add useful internal links.
7. Update `02 - Wiki/index.md`.
8. Append one entry to `02 - Wiki/log.md`.
9. Report:
   - source reviewed
   - pages created
   - pages updated
   - conflicts found
   - open questions

## Query workflow

When asked a question:

1. Read `02 - Wiki/index.md` first.
2. Open the smallest useful set of wiki pages.
3. Answer from the wiki.
4. If the answer creates reusable knowledge, save it back into the wiki.
5. Update `02 - Wiki/index.md` if a new page was added.
6. Append `02 - Wiki/log.md` if the new page is a meaningful addition.

## Lint workflow

When asked to lint the wiki:

- find orphan pages
- find thin pages with little value
- find duplicate pages
- find stale claims
- find broken or weak links
- find pages that should be merged
- find pages in the wrong folder
- find project notes that should become wiki knowledge
- find wiki pages that belong in archive

## What not to do

- do not store secrets in the wiki
- do not store passwords or API keys
- do not keep duplicate drafts in many folders
- do not turn daily notes into wiki pages unless they contain lasting value
- do not create empty pages just to fill a structure
- do not make giant pages mixing many topics

## Good page shape

A strong page usually has:

- short summary
- key facts
- links to related pages
- source or source-note links
- open questions if needed
- last updated date

## Naming rules

Use clear names.

Examples:
- `Swiss School Buyer Notes`
- `WortStart Positioning`
- `German DaZ Support`
- `Client Onboarding Process`
- `Jeta Distributions`

Avoid vague names like:
- `notes`
- `ideas`
- `stuff`
- `meeting`
- `random`

## Index rule

`02 - Wiki/index.md` is the top route into the wiki.

It should point to:
- major topics
- key hub pages
- major companies
- major projects
- core processes

Update it when the wiki gains a new useful area.

## Log rule

`02 - Wiki/log.md` is the running change log.

Append one short entry for:
- each ingest
- each major query saved into the wiki
- each lint pass with meaningful cleanup