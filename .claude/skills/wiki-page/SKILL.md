---
name: wiki-page
description: Create or update one wiki page on a named topic.
context: fork
agent: wiki-writer
disable-model-invocation: true
---

Create or update one wiki page for this topic: $ARGUMENTS

Steps:
1. Read `02 - Wiki/index.md`.
2. Check if a close page already exists.
3. Update that page, or create one if needed.
4. Add links to related pages.
5. Update `02 - Wiki/index.md` if this is a new key page.
6. Append `02 - Wiki/log.md` if the change is major.

Keep the page short, linked, and reusable.