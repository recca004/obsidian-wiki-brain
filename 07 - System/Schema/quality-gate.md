# Quality Gate

This file defines the checks that should happen before a wiki change is treated as good enough to keep.

## Goal

Keep the wiki clean, useful, and stable.

The quality gate should stop:
- duplicate pages
- weak page names
- missing frontmatter
- bad links
- poor file placement
- source-less claims
- giant messy pages
- raw source edits

---

## When to Run the Quality Gate

Run the quality gate:
- after ingest
- after a major page update
- after new page creation
- after a merge
- after a rename
- before large cleanup work is treated as done

For small edits, a light pass is enough.

---

## Pass / Fix / Stop

Each check should end with one of these:

- `pass` = good, no change needed
- `fix` = issue found, but easy to correct now
- `stop` = do not continue until fixed

Use `stop` for:
- raw source edits
- missing required frontmatter
- clear duplicate pages
- broken structure after rename or merge
- false certainty on weak facts
- secrets or credentials in the wiki

---

## 1. File Placement Check

Ask:
- is the page in the right folder
- is this wiki knowledge or only project work
- is this a map, concept, process, project, company, person, glossary, source-note, daily, or workbench note

### Pass
- page is in the correct folder

### Fix
- page belongs in another folder but content is still useful

### Stop
- raw source was moved into the wiki as if it were final knowledge
- live task or scratch work was saved as stable wiki knowledge

---

## 2. Page Type Check

Ask:
- does the page have one clear type
- does the content match the type
- does the page try to be many types at once

### Pass
- one clear type
- content matches that type

### Fix
- type is right but content needs cleanup

### Stop
- no clear type
- page mixes many topics and cannot be understood as one page

---

## 3. Frontmatter Check

Check:
- `type`
- `status`
- `created`
- `updated`

Use the schema rules in `frontmatter-rules.md`.

### Pass
- required fields exist
- dates use `YYYY-MM-DD`
- values match allowed schema

### Fix
- missing alias or tag where it would help
- `updated` not refreshed after a major edit

### Stop
- missing required frontmatter
- bad date format
- unknown type value

---

## 4. Naming Check

Ask:
- is the page name clear
- would a future search find this easily
- is the name too vague or too generic

### Pass
- name is clear and specific

### Fix
- name can be improved for clarity

### Stop
- vague names like:
  - `notes`
  - `stuff`
  - `meeting`
  - `ideas`
  - `random`

---

## 5. Duplicate Check

Ask:
- does a page already exist on this topic
- is this only a slight rewording of another page
- should this content be merged into an existing page

### Pass
- topic is clearly distinct

### Fix
- overlap exists, but one page can be merged or renamed

### Stop
- near-duplicate page was created when a good page already existed

---

## 6. Summary Check

Ask:
- does the page explain itself near the top
- can a reader understand the topic fast
- is there a short summary

### Pass
- short summary exists

### Fix
- summary is weak or too long

### Stop
- no clear summary and page cannot be understood quickly

---

## 7. Structure Check

Ask:
- does the page have clean sections
- is one topic kept on one page
- is the page easy to scan

### Pass
- sections are clear
- one topic per page

### Fix
- sections need cleanup
- a few items belong elsewhere

### Stop
- giant mixed page with many unrelated topics

---

## 8. Link Check

Use `link-rules.md`.

Ask:
- does the page link to useful related pages
- is the page isolated
- are there broken or weak links
- is link density reasonable

### Pass
- page has useful internal links
- no broken structure links

### Fix
- page needs more links
- map pages or related pages block should be updated

### Stop
- stable page has no route into the wiki
- major broken links after rename or merge

---

## 9. Source Check

Ask:
- where did the facts come from
- does the page link to source summary pages when needed
- are facts stated too strongly without support

### Pass
- source notes are linked where needed
- claims are grounded

### Fix
- source links should be added
- weak claims should be marked as open questions

### Stop
- unsupported factual claims are written as certain
- raw source text is pasted into many pages without need

---

## 10. Reuse Check

Ask:
- will this page still help later
- is this long-term knowledge
- should this stay in workbench, daily, or project space instead

### Pass
- page has clear reuse value

### Fix
- page has value but needs cleanup before it belongs in the wiki

### Stop
- page is only temporary scratch work or task noise

---

## 11. Map and Index Check

Ask:
- should this page be added to a map
- should this page be added to the main index
- is this a new entry point into a topic

### Pass
- page is already reachable through index or map when needed

### Fix
- update a map page
- update `02 - Wiki/index.md`

### Stop
- a major new topic was added with no route from index or maps

---

## 12. Log Check

Ask:
- was this a meaningful change
- should `02 - Wiki/log.md` be updated

### Pass
- log updated when needed

### Fix
- add missing log entry

### Stop
- large structural change made with no log entry

---

## 13. Raw Source Protection Check

Ask:
- was anything in `01 - Raw Sources/` edited
- was the source kept intact

### Pass
- raw source unchanged

### Stop
- raw source edited after capture

Rule:
Raw sources are read-only once saved.

---

## 14. Secret Check

Ask:
- does the page include passwords
- API keys
- private tokens
- secret client data that should not live here

### Pass
- no secrets found

### Stop
- any secret or credential is found in the wiki

Rule:
Secrets do not belong in the wiki.

---

## 15. Date Check

Ask:
- are frontmatter and system dates in `YYYY-MM-DD`
- are body text dates clear
- is date style mixed inside frontmatter

### Pass
- frontmatter uses `YYYY-MM-DD`
- note body may use Swiss-style display dates when useful

### Fix
- clean mixed date style in note body if it causes confusion

### Stop
- frontmatter uses mixed or wrong date format

---

## 16. Final Gate

A page or change is good enough when:

- folder is correct
- page type is clear
- frontmatter is valid
- title is clear
- duplicate risk is low
- summary exists
- structure is readable
- links are useful
- source grounding is good enough
- index or map path exists when needed
- log is updated when needed
- no raw source edit happened
- no secrets are present

---

## Quick Quality Checklist

Use this fast checklist after a write:

- right folder
- right page type
- frontmatter valid
- clear title
- short summary
- no duplicate page
- useful internal links
- source notes linked
- index updated if needed
- log updated if needed

If all are true, the page can pass.

---

## Agent Rules

### Manager agent
Should:
- decide whether a change is ready to pass
- stop weak new page creation
- send cleanup work to the linter
- send writing fixes to the writer

### Research subagent
Should:
- check for duplicate topics
- check source support
- find weak claims and missing links

### Writer subagent
Should:
- fix frontmatter
- fix structure
- add links
- update index and log
- avoid raw source edits

### Linter subagent
Should:
- run broad quality checks
- flag orphan pages
- flag weak page names
- flag wrong folder placement
- flag missing index or map routes

---

## Output Format for Quality Gate Runs

When reporting a quality gate result, use:

- overall result: pass / fix / stop
- files checked
- issues found
- fixes made
- fixes still needed
- open questions

### Example

- overall result: fix
- files checked:
  - `02 - Wiki/Projects/WortStart.md`
- issues found:
  - missing source links
  - `updated` date not refreshed
- fixes made:
  - added `Source Notes` section
- fixes still needed:
  - add link from `Learning Map`
- open questions:
  - none

---

## Success Check

The quality gate is working when:
- weak pages get caught early
- duplicate pages stay low
- map and index routes stay clean
- source grounding stays visible
- raw sources stay untouched
- the wiki stays useful as it grows