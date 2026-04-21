---
name: wiki-ingest
description: Ingest one raw source into the wiki.
context: fork
agent: wiki-writer
disable-model-invocation: true
---

Ingest this source into the wiki: $ARGUMENTS

Steps:
1. Read the source fully.
2. Read `02 - Wiki/index.md`.
3. Find related pages.
4. Update existing pages first.
5. Create new pages only when needed.
6. Add internal links.
7. Update `02 - Wiki/index.md`.
8. Append one log entry to `02 - Wiki/log.md`.

Return:
- pages created
- pages updated
- conflicts found
- open questions