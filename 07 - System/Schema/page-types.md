# Page Types

This file defines the page types used in the wiki.

## Goal

Keep page structure clean and stable.

Each page should have:
- one main purpose
- one clear page type
- predictable frontmatter
- clean internal links

---

## 1. Concept Page

**Use for:**
- ideas
- methods
- frameworks
- topics
- market or domain knowledge

**Folder:**
- `02 - Wiki/Concepts/`

**Required frontmatter:**
- `type: concept`
- `status`
- `created`
- `updated`

**Suggested sections:**
- Summary
- Key Points
- Why It Matters
- Related Pages
- Open Questions
- Source Notes

**Examples:**
- `Swiss School Market`
- `Role-Based Access`
- `German DaZ Support`

---

## 2. Company Page

**Use for:**
- companies
- brands
- agencies
- products treated like business entities

**Folder:**
- `02 - Wiki/Companies/`

**Required frontmatter:**
- `type: company`
- `status`
- `created`
- `updated`

**Suggested sections:**
- Summary
- Core Facts
- Offer
- Audience
- Related Projects
- Related Pages
- Open Questions
- Source Notes

**Examples:**
- `DigitalSolace`
- `Jeta Distributions`

---

## 3. Person Page

**Use for:**
- people you work with
- clients
- partners
- thought leaders tied to the wiki

**Folder:**
- `02 - Wiki/People/`

**Required frontmatter:**
- `type: person`
- `status`
- `created`
- `updated`

**Suggested sections:**
- Summary
- Role
- Related Companies
- Related Projects
- Notes
- Source Notes

**Examples:**
- `Mario N`
- `Client Contact - Jeta`

---

## 4. Process Page

**Use for:**
- repeatable workflows
- internal operating methods
- checklists with lasting value

**Folder:**
- `02 - Wiki/Processes/`

**Required frontmatter:**
- `type: process`
- `status`
- `created`
- `updated`

**Suggested sections:**
- Goal
- Trigger
- Inputs
- Steps
- Output
- Common Mistakes
- Related Pages
- Source Notes

**Examples:**
- `Client Onboarding Process`
- `Product Vision Workflow`

---

## 5. Project Knowledge Page

**Use for:**
- stable knowledge about one project
- scope
- rules
- architecture
- product decisions
- long-term notes worth keeping

**Folder:**
- `02 - Wiki/Projects/`

**Required frontmatter:**
- `type: project`
- `status`
- `created`
- `updated`

**Suggested sections:**
- Summary
- Goal
- Scope
- Decisions
- Key Facts
- Related Companies
- Related Processes
- Open Questions
- Source Notes

**Examples:**
- `WortStart`
- `WishlistApp`

---

## 6. Glossary Page

**Use for:**
- terms
- short definitions
- acronyms
- naming rules

**Folder:**
- `02 - Wiki/Glossary/`

**Required frontmatter:**
- `type: glossary`
- `status`
- `created`
- `updated`

**Suggested sections:**
- Definition
- Notes
- Related Pages
- Source Notes

**Examples:**
- `DaZ`
- `CPT`
- `CCT`

---

## 7. Map Page

**Use for:**
- route pages
- hub pages
- entry pages for one topic area

**Folder:**
- `03 - Maps/`

**Required frontmatter:**
- `type: map`
- `status`
- `created`
- `updated`

**Suggested sections:**
- Scope
- Main Pages
- Related Areas
- Open Gaps

**Examples:**
- `Companies`
- `Projects`
- `Processes`

---

## 8. Source Summary Page

**Use for:**
- one source distilled into useful notes
- source facts without copying the full raw source into the wiki

**Folder:**
- `02 - Wiki/Sources/`

**Required frontmatter:**
- `type: source-note`
- `status`
- `created`
- `updated`
- `source_path`

**Suggested sections:**
- Summary
- Key Facts
- Decisions
- People
- Companies
- Related Pages
- Open Questions

**Examples:**
- `Source - WortStart Product Brief`
- `Source - Client Emailing Process Draft`

---

## 9. Index Page

**Use for:**
- the main entry page into the wiki
- links to major areas
- links to key map pages
- links to high-value pages

**File:**
- `02 - Wiki/index.md`

**Required frontmatter:**
- `type: index`
- `status`
- `created`
- `updated`

**Rule:**
The index is short and focused.
It does not list every page in the vault.

---

## 10. Log Page

**Use for:**
- append-only record of major wiki operations
- ingest records
- major structural changes
- major saved query outputs
- cleanup records

**File:**
- `02 - Wiki/log.md`

**Required frontmatter:**
- `type: log`
- `status`
- `created`
- `updated`

**Rule:**
The log should be short, parseable, and chronological.

---

## 11. Daily Note

**Use for:**
- day planning
- scratch notes
- quick captures

**Folder:**
- `06 - Daily/`

**Required frontmatter:**
- `type: daily`
- `date`

**Rule:**
Daily notes are not part of the long-term wiki unless useful knowledge gets promoted into the wiki.

---

## 12. Workbench Note

**Use for:**
- temporary thinking
- rough drafts
- raw planning
- unfinished notes

**Folder:**
- `04 - Workbench/`

**Required frontmatter:**
- `type: workbench`
- `status`
- `created`
- `updated`

**Rule:**
Workbench notes are temporary. Good content should be moved into a proper wiki page later.

---

## Promotion Rule

Move a note into the wiki when it has:
- lasting value
- clean structure
- one clear topic
- links to other pages

Keep a note out of the wiki when it is:
- temporary
- task-only
- duplicate
- unclear
- unfinished

---

## Status Values

Use one of these:
- `active`
- `draft`
- `stable`
- `archived`

---

## Type List

Allowed `type` values:
- `concept`
- `company`
- `person`
- `process`
- `project`
- `glossary`
- `map`
- `source-note`
- `index`
- `log`
- `daily`
- `workbench`