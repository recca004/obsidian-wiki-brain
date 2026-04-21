---
name: wiki-query
description: Research a topic in the wiki and return a grounded answer.
context: fork
agent: wiki-researcher
disable-model-invocation: true
---

Answer this from the vault: $ARGUMENTS

Steps:
1. Read `02 - Wiki/index.md`.
2. Open the smallest useful set of related pages.
3. Pull out facts, links, gaps, and conflicts.
4. Return a short answer with file paths.
5. If the answer shows a clear knowledge gap, say which page should be added or updated.