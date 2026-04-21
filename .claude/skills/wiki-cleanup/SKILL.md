---
name: wiki-cleanup
description: Check the vault for wiki quality issues.
context: fork
agent: wiki-linter
disable-model-invocation: true
---

Run a wiki cleanup pass.

Check:
- duplicate pages
- orphan pages
- weak links
- stale claims
- pages in the wrong folder
- project notes that should move into the wiki
- wiki pages that should move to archive

Return:
- highest-value fixes first
- file paths for every finding
- merge or move notes where useful