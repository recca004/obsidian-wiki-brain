# Ingest Rules

This file defines how a source moves from raw capture into the wiki.

## Goal

Turn one source into clean, linked knowledge without making duplicates or messy pages.

The ingest process should:
- keep raw sources untouched
- pull out useful facts
- update existing pages first
- create new pages only when needed
- add links
- update the index and log
- leave a short report

---

## Core Ingest Flow

The standard ingest flow is:

1. locate the source
2. read the source fully
3. identify the main topic
4. pull out facts and decisions
5. identify related pages
6. update existing pages first
7. create new pages only when needed
8. add useful links
9. update index if needed
10. append log entry
11. return a short report

---

## 1. Allowed Source Locations

Sources usually come from:

- `01 - Raw Sources/`
- `04 - Workbench/`
- `06 - Daily/`

Rule:
If the note is still rough, do not treat it as final wiki knowledge.

---

## 2. Raw Source Protection

If the source is in `01 - Raw Sources/`:

- read it
- do not edit it
- do not rewrite it in place
- do not turn it into a live wiki page by editing the source file itself

Rule:
Raw sources are read-only once saved.

---

## 3. Read the Full Source

Before any write:

- read the full source
- do not work from only the title
- do not work from one short section if the source is longer
- do not guess the full meaning from a partial scan

The source should be understood before pages are changed.

---

## 4. Pull Out the Right Material

During ingest, identify:

- main topic
- facts
- decisions
- people
- companies
- processes
- projects
- terms
- open questions
- conflicts with older notes

Do not copy large chunks of raw source text into the wiki.

Pull out reusable knowledge.

---

## 5. Decide if a Source Summary Page Is Needed

Create a source summary page when:

- the source is rich and likely to matter later
- many wiki pages may rely on it
- the source contains key decisions
- the source will be used as evidence later

A source summary page should:
- stay shorter than the raw source
- pull out key facts and decisions
- link to related wiki pages
- keep a clear `source_path`

If the source is small and low value, a separate source summary page may not be needed.

---

## 6. Check Existing Pages First

Before creating anything new:

1. read `02 - Wiki/index.md`
2. check close matches in the wiki
3. check related map pages
4. check project, concept, process, company, person, and glossary pages that may already cover the topic

Rule:
Update first. Create second.

---

## 7. Update Existing Pages First

If a good page already exists:

- add the new facts there
- add source links
- update `updated`
- add links to related pages
- mark new open questions if needed

Do not split one topic across many weak pages.

---

## 8. Create a New Page Only When Needed

Create a new page only when:

- the topic is clearly distinct
- there is lasting value
- the content has one main focus
- no existing page already covers it well

New page types should follow `page-types.md` and `frontmatter-rules.md`.

---

## 9. Place New Pages in the Right Folder

Use these destinations:

- concept -> `02 - Wiki/Concepts/`
- company -> `02 - Wiki/Companies/`
- person -> `02 - Wiki/People/`
- process -> `02 - Wiki/Processes/`
- project -> `02 - Wiki/Projects/`
- glossary -> `02 - Wiki/Glossary/`
- map -> `03 - Maps/`
- source-note -> `02 - Wiki/Sources/` or a nearby topic area if that is your chosen layout

Do not place long-term wiki pages in:
- `04 - Workbench/`
- `06 - Daily/`

---

## 10. Frontmatter Rule During Ingest

Every long-term page created or touched during ingest should follow the frontmatter schema.

At minimum, long-term pages should have:

- `type`
- `status`
- `created`
- `updated`

Use:
- `YYYY-MM-DD` for frontmatter dates
- Swiss-style display dates only in note body when useful

---

## 11. Link Rule During Ingest

After updates are made:

- link the changed page to related pages
- add source summary links where useful
- update map pages if the topic area is growing
- avoid weak link stuffing

Good ingest leaves pages more connected than before.

---

## 12. Index Update Rule

Update `02 - Wiki/index.md` only when the ingest creates or strengthens:

- a major concept page
- a major project page
- a new map page
- a high-value entry point

Do not add every page to the main index.

---

## 13. Log Update Rule

Append `02 - Wiki/log.md` when the ingest causes:

- a source review
- a new high-value page
- a major page update
- a rename
- a merge
- a cleanup pass tied to the ingest

A log entry should be short and clear.

Good log entry shape:

- date
- source
- pages changed
- short note

---

## 14. Conflicts Rule

If the source conflicts with older wiki content:

- do not hide the conflict
- do not overwrite older facts without care
- mark the conflict clearly
- update the page with an open question or note on the conflict
- link to the source summary page when useful

If needed, add a short section like:

## Open Questions

- Source A says one thing.
- Older project page says another.
- This needs review.

---

## 15. Promotion Rule During Ingest

Promote information into the wiki when it is:

- stable enough
- useful later
- tied to a clear topic
- worth linking to again

Keep information out of the wiki when it is:

- rough scratch work
- passing task noise
- personal reminder text with no reuse value
- duplicate material already covered well elsewhere

---

## 16. Ingest Output Report

Every ingest should end with a short report.

Use this shape:

- source reviewed
- source summary created or not
- pages created
- pages updated
- pages renamed
- pages merged
- conflicts found
- open questions

### Example

- source reviewed:
  - `01 - Raw Sources/_Inbox/2026-04-20-wortstart-product-brief.md`
- source summary created:
  - `02 - Wiki/Sources/Source - WortStart Product Brief.md`
- pages created:
  - `02 - Wiki/Projects/WortStart.md`
- pages updated:
  - `02 - Wiki/Concepts/Swiss School Market.md`
- pages renamed:
  - none
- pages merged:
  - none
- conflicts found:
  - none
- open questions:
  - buyer detail still needs confirmation

---

## 17. Light Ingest vs Full Ingest

### Light ingest

Use when:
- the source is small
- the value is narrow
- only one or two pages need updates

Light ingest may:
- skip a source summary page
- update one or two pages
- add a short log entry

### Full ingest

Use when:
- the source is rich
- many pages are touched
- the source may matter later
- the source adds project, process, and concept knowledge

Full ingest should:
- review source fully
- create a source summary page when useful
- update all key related pages
- update map pages if needed
- update index if needed
- append log entry
- return a full report

---

## 18. Bad Ingest Patterns

Do not:

- edit raw source files
- copy raw source text into many pages
- create a new page before checking existing pages
- create vague pages with weak names
- skip source links for key claims
- skip the log after major ingest work
- add every new page to the main index
- split one topic across many thin notes
- turn daily notes into wiki pages without cleanup

---

## 19. Agent Roles During Ingest

### Manager agent

Should:
- decide light ingest or full ingest
- decide if a source summary page is needed
- stop duplicate page creation
- decide when index and log updates are needed

### Research subagent

Should:
- read the source
- identify facts, decisions, people, companies, projects, and processes
- find related pages
- flag conflicts and gaps

### Writer subagent

Should:
- update existing pages first
- create new pages when needed
- add links
- update frontmatter
- update index and log when needed

### Linter subagent

Should:
- check duplicate risk
- check broken links after changes
- check wrong folder placement
- check weak page names and thin pages

---

## 20. Ingest Success Check

An ingest is good when:

- the source stayed untouched
- the topic was understood
- the right pages were updated
- duplicate pages were avoided
- new pages were created only when needed
- links improved
- source grounding stayed visible
- index stayed clean
- log was updated when needed
- the report is short and clear