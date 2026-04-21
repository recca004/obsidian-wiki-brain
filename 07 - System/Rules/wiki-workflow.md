# Wiki Workflow

This file defines how work should move through the wiki.

It is the operating workflow for the manager agent and all wiki subagents.

## Goal

Turn raw material into clean, linked, reusable knowledge.

The workflow should:
- keep raw sources separate
- keep the wiki clean
- stop duplicate pages
- keep links useful
- keep the index and log up to date

---

## Core Flow

The main wiki flow is:

1. capture source
2. place source in raw storage
3. review source
4. check existing wiki pages
5. update or create wiki pages
6. add links
7. update index
8. update log
9. run cleanup when needed

---

## 1. Capture

New material can come from:
- notes
- research
- meetings
- client calls
- project docs
- copied text
- voice note transcripts
- daily notes
- workbench notes

Rule:
New material should enter the system first as raw input or temporary work, not as final wiki knowledge.

---

## 2. Raw Storage

Raw material belongs in:

- `01 - Raw Sources/`
- `04 - Workbench/`
- `06 - Daily/`

Use:
- `01 - Raw Sources/` for source files and stable captures
- `04 - Workbench/` for rough thinking
- `06 - Daily/` for day-based notes

Rule:
Do not treat rough notes as finished wiki pages.

---

## 3. Review

Before writing to the wiki:

1. read the source fully
2. identify the main topic
3. pull out facts
4. pull out decisions
5. pull out people, companies, projects, and processes
6. pull out open questions
7. check whether this note has lasting value

Questions to ask:
- is this reusable later
- is this one clear topic
- does a page already exist
- should this stay in workbench only
- should this become a source summary page

---

## 4. Decide the Page Type

Choose the page type before writing.

Use:
- `concept` for ideas, methods, frameworks, market knowledge
- `company` for brands, companies, agencies
- `person` for people
- `process` for repeatable workflows
- `project` for stable project knowledge
- `glossary` for terms and short definitions
- `map` for route pages
- `source-note` for distilled source summaries

Rule:
Do not create pages without a clear type.

---

## 5. Check Existing Pages First

Before making a new page:

1. search for the topic
2. check close page names
3. check related map pages
4. check the index
5. update an existing page if it already covers the topic

Rule:
Update first. Create second.

This keeps the wiki from splitting into near-duplicate pages.

---

## 6. Write or Update the Wiki Page

When writing a page:

- keep one main topic per page
- use the right frontmatter
- write a short summary
- keep key facts clear
- add related links
- add source links when useful
- mark unclear points as open questions

A strong page should be:
- short
- readable
- linked
- reusable
- easy to update later

---

## 7. Add Internal Links

After writing or updating a page:

- link to related concept pages
- link to related project pages
- link to related company or person pages
- link to source summary pages when needed
- update map pages if the topic area is growing

Rule:
Add useful links, not many links.

---

## 8. Update the Index

Update `02 - Wiki/index.md` when:
- a new major area appears
- a new map page is added
- a high-value project page is created
- a key concept page becomes an entry point

Do not add every page to the index.

The index is for:
- main areas
- key maps
- major entry pages

---

## 9. Update the Log

Append to `02 - Wiki/log.md` when:
- a source is ingested
- a major wiki page is created
- a major wiki page is updated
- a cleanup pass changes the structure
- a merge or rename is done

Each log entry should be short.

Include:
- date
- action
- main page or area changed

---

## 10. Query Workflow

When answering a question from the wiki:

1. read `02 - Wiki/index.md`
2. open the smallest useful set of pages
3. answer from the existing wiki
4. note gaps or conflicts
5. save reusable answers back into the wiki when useful
6. update the index and log if a new lasting page is created

Rule:
Do not turn every answer into a page.
Only save answers that have lasting reuse value.

---

## 11. Ingest Workflow

When ingesting one source:

1. open the raw source
2. make a source summary if needed
3. identify related wiki pages
4. update existing pages first
5. create new pages only when the topic is distinct
6. add links
7. update the index if needed
8. append the log
9. report:
   - source reviewed
   - pages created
   - pages updated
   - conflicts found
   - open questions

---

## 12. Lint Workflow

Run lint when:
- the wiki grows
- many pages were added
- pages were renamed
- topic areas feel messy
- links feel weak

Check for:
- orphan pages
- thin pages
- duplicate pages
- stale claims
- broken or weak links
- wrong folder placement
- project notes that belong in the wiki
- wiki pages that belong in archive

Rule:
Lint should improve structure, not just count problems.

---

## 13. Promotion Rule

Promote a note into the wiki when it has:
- lasting value
- one clear topic
- clean enough structure
- real reuse potential
- clear links to other knowledge

Keep a note out of the wiki when it is:
- temporary
- task-only
- rough
- unclear
- duplicate
- personal scratch work with no later value

---

## 14. Rename Rule

Rename a page when:
- the name is vague
- the page title no longer matches the topic
- two pages need clearer separation
- the title is too short or unclear

After renaming:
1. keep the new name clear
2. add aliases when needed
3. check backlinks
4. check map pages
5. check the index
6. fix weak links

---

## 15. Merge Rule

Merge pages when:
- two pages cover the same topic
- one is much thinner
- one title is weak
- the split no longer helps navigation

When merging:
1. keep the stronger title
2. move useful content into one page
3. keep aliases if needed
4. fix major links
5. archive or remove the weaker duplicate based on system rules

---

## 16. Archive Rule

Archive pages when:
- they are no longer active
- they are outdated and replaced
- they are duplicates kept only for history
- they are no longer useful in current navigation

Archive pages should not become the main route into a topic.

---

## 17. Agent Roles

### Main manager agent

The manager agent should:
- decide whether to work directly or delegate
- choose the right page type
- protect structure
- stop duplicate page creation
- keep index and log habits steady

### Research subagent

The research subagent should:
- read sources
- compare pages
- trace facts
- find related pages
- find gaps and conflicts

### Writer subagent

The writer subagent should:
- update wiki pages
- create new pages when needed
- add links
- update index and log
- keep writing clean and short

### Linter subagent

The linter subagent should:
- find structure problems
- find duplicates
- find orphan pages
- find stale or weak pages
- suggest merges, moves, and cleanup

---

## 18. Daily Working Pattern

A clean daily pattern is:

1. capture notes in daily or raw
2. move useful sources into raw storage
3. ingest one source at a time
4. update linked wiki pages
5. keep active project work in `05 - Projects/`
6. move only lasting knowledge into `02 - Wiki/`
7. run lint from time to time

---

## 19. What Not to Do

Do not:
- dump chats into the wiki
- turn every note into a page
- create empty structure pages
- keep many near-duplicate pages
- use daily notes as long-term knowledge storage
- link every repeated word
- mix raw source text into many wiki pages
- skip the index and log on major changes

---

## 20. Success Check

The wiki is working well when:
- new sources become linked knowledge fast
- pages are easy to find
- duplicate pages stay low
- map pages help movement
- the index stays short and useful
- the log shows real progress
- answers can be built from the wiki without re-reading everything