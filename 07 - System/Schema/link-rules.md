# Link Rules

This file defines how pages should link to each other.

## Goal

Make the wiki easy to move through.

Links should:
- connect related knowledge
- reduce duplicate notes
- help the index and map pages stay useful

---

## Main Rule

Use internal links as the main way to connect the wiki.

Use this format:

[[Page Name]]

Use aliases when needed:

[[Page Name|Shown Text]]

---

## When to Link

Add a link when:
- the other page is directly relevant
- the other page helps explain the current page
- the link connects concept, project, process, person, or company knowledge
- the link helps future search and reuse

Do not add links just to raise link count.

---

## Good Linking Pattern

A strong page often links to:
- one parent idea or map
- two to five close related pages
- one or more source summary pages when useful

---

## Link Directions

Try to keep links natural in both directions.

If page A links to page B many times, page B should often link back to A when it makes sense.

This helps:
- backlink views
- related page discovery
- cleaner movement across the wiki

---

## Map Pages

Use map pages as route pages, not storage pages.

A map page should link to:
- main pages in one area
- key concept pages
- key project pages
- open gaps

A map page should not:
- repeat full page content
- become a giant dump of links
- replace the index page

---

## Index Page

`02 - Wiki/index.md` should link only to:
- major areas
- key maps
- top pages
- high-value entry points

Do not put every page in the index.

---

## Source Links

When a wiki page is shaped by one or more sources, add links to the source summary pages in a `Source Notes` section.

Like this:

## Source Notes

- [[Source - WortStart Product Brief]]
- [[Source - Client Call 2026-04-20]]

Do not copy raw source text into many pages.

---

## New Page Rule

Before making a new page:
1. search for an existing page on the same topic
2. update that page if it already exists
3. create a new page only when the topic is clearly distinct

This avoids near-duplicate pages.

---

## Alias Rule

Use aliases when:
- a page has a known short name
- a term has more than one spelling
- people may search using another label

Do not use aliases to hide poor page naming.

Bad page name:
- `notes 1`

Good page name:
- `Swiss School Market`

---

## Link Density

Aim for useful links, not many links.

Good:
- 3 to 8 strong links on a normal page

Too few:
- 0 or 1 link on a mature page

Too many:
- a link on nearly every line

Use judgment.

---

## Orphan Page Rule

A page should not stay orphaned unless it is:
- brand new
- a temporary workbench note
- an archive page

A wiki page is weak when:
- nothing links to it
- it links to nothing
- it has no map or index path

---

## Broken Link Rule

Do not leave broken links in stable pages.

When a page is renamed:
- fix incoming links if needed
- keep aliases when useful
- check map pages
- check the index page

---

## Section-Level Link Pattern

A strong wiki page often links in these places:
- Summary
- Related Pages
- Source Notes
- Open Questions

You do not need links in every section.

---

## Preferred Link Targets

Prefer linking to:
- stable wiki pages
- map pages for broad topics
- source summary pages for evidence

Avoid linking from stable pages to:
- rough scratch notes
- throwaway workbench notes
- old archive pages unless there is a clear reason

---

## Cross-Type Linking Rules

Good cross-links:

- concept -> project
- project -> process
- project -> company
- process -> concept
- person -> company
- company -> project
- glossary -> concept
- map -> all key page types in that area

These links make the wiki more useful than folder-only storage.

---

## Source Note Linking Rule

A source summary page should link out to:
- the main project or concept it supports
- any people or companies named in the source
- related process pages when the source changes how work is done

A source summary page should not try to become the final knowledge page.
It supports the wiki. It does not replace it.

---

## Map Coverage Rule

When a topic grows past 4 to 6 connected pages, it may need a map page.

A map page is useful when:
- one topic now has many related pages
- you need one place to enter that area
- the topic has concepts, projects, people, and sources tied together

Do not make map pages too early.

---

## Index Coverage Rule

A new page should go into `02 - Wiki/index.md` only when it is:
- a major entry point
- a high-value project page
- a key concept page
- a map page
- a page you expect to reuse often

Most pages should not go straight into the main index.

---

## Rename Rule

When a page is renamed:
1. keep the new title clear and stable
2. add the old name as an alias if still useful
3. check map pages
4. check the main index
5. check backlinks
6. fix weak references in major pages

---

## Merge Rule

Merge pages when:
- two pages cover the same topic
- one page is much thinner than the other
- titles differ but the content is the same
- the split no longer helps navigation

When merging:
- keep the stronger title
- move useful content over
- add aliases if needed
- update major links
- archive or delete the weaker duplicate based on your system rule


---

## Relationship Blocks

When useful, add a short `## Related Pages` block near the end of the page.

Use this format:

## Related Pages

- [[WortStart]]
- [[Swiss School Market]]
- [[German DaZ Support]]

Keep it short.
Only list real related pages.

---

## Link Text Rule

Prefer clean page titles in links.

Good:
- [[WortStart]]
- [[Swiss School Market]]

Use alias display text only when it reads better in the sentence.

Good:
- [[Swiss School Market|the Swiss school market]]

Avoid hiding page titles too much with custom display text.

---

## Workbench and Daily Note Rule

Stable wiki pages should not depend on:
- daily notes
- workbench notes
- random scratch pages

If a daily or workbench note contains lasting value:
1. move that knowledge into a proper wiki page
2. link the daily note to the new page if needed
3. do not keep the daily note as the only route to the idea

---

## Archive Linking Rule

Archive pages can be linked when needed for history or context.

Still:
- do not make archive pages central to current navigation
- do not send new readers into archive pages first
- prefer live pages when both exist

---

## What to Avoid

Do not:
- link every repeated word
- make pages only to satisfy one link
- use raw URLs as internal wiki structure
- keep duplicate pages with slightly different names
- leave source-heavy pages with no route back into the wiki
- link stable pages mainly to temporary notes
- stuff a page with long lists of weak links

---

## Agent Rules

Agents should:
- read `02 - Wiki/index.md` before broad wiki tasks
- check for an existing page before creating a new one
- add links during page updates
- flag orphan pages during lint runs
- update map pages when a new topic area becomes real
- keep the index focused and short
- prefer updating a good existing page over creating a near-duplicate
- add source summary links when a claim comes from a named source

---

## Link Examples

### Good

WortStart is linked to [[Swiss School Market]] and [[German DaZ Support]].

See also [[Client Onboarding Process]].

## Related Pages

- [[WortStart]]
- [[WishlistApp]]
- [[DigitalSolace]]

### Weak

This project is about school and app and market and teaching and product.

That line should have real page links if those pages exist.