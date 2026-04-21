# Frontmatter Rules

This file defines the frontmatter rules for the wiki.

## Goal

Keep metadata simple, stable, and easy for agents to read.

---

## Base Rule

Every long-term wiki page and named system page should start with YAML frontmatter.

Use this at the top of the file:

```yaml
---
type: concept
status: active
created: 2026-04-20
updated: 2026-04-20
aliases: []
tags: []
---
```

---

## Core Fields

### 1. `type`

**Required:** yes

Allowed values:
- `concept`
- `company`
- `person`
- `process`
- `project`
- `glossary`
- `map`
- `source-note`
- `daily`
- `workbench`

---

### 2. `status`

**Required:** yes for long-term pages

Allowed values:
- `draft`
- `active`
- `stable`
- `archived`

Use:
- `draft` for early pages
- `active` for working pages
- `stable` for pages that do not change much
- `archived` for old pages kept for reference

---

### 3. `created`

**Required:** yes

Format:
- `YYYY-MM-DD`

This is the first creation date of the page.

---

### 4. `updated`

**Required:** yes

Format:
- `YYYY-MM-DD`

Change this whenever the page gets a meaningful update.

---

### 5. `aliases`

**Required:** no  
**Recommended:** yes when a page may be searched under other names

Format:

```yaml
aliases:
  - Alt Name
  - Short Name
```

Use aliases for:
- short forms
- old names
- alternate spellings
- acronyms

---

### 6. `tags`

**Required:** no

Format:

```yaml
tags:
  - schools
  - product
  - research
```

Rule:
- keep tags few
- use them for broad grouping only
- do not use tags as the main navigation system

---

## Optional Fields

Use only when needed.

### `source_path`

Use on source summary pages.

```yaml
source_path: "01 - Raw Sources/_Inbox/2026-04-20-wortstart-product-brief.md"
```

---

### `source_date`

Use when the source itself has a date.

```yaml
source_date: 2026-04-20
```

---

### `owner`

Use for project or process pages when a person or team owns the area.

```yaml
owner: Mario N
```

---

### `related`

Use when you want a clean list of main related pages.

```yaml
related:
  - "[[WortStart]]"
  - "[[Swiss School Market]]"
```

Do not overuse this. Normal page links are still the main method.

---

## Frontmatter by Page Type

## Concept Page

```yaml
---
type: concept
status: active
created: 2026-04-20
updated: 2026-04-20
aliases: []
tags: []
---
```

## Company Page

```yaml
---
type: company
status: active
created: 2026-04-20
updated: 2026-04-20
aliases: []
tags: []
---
```

## Person Page

```yaml
---
type: person
status: active
created: 2026-04-20
updated: 2026-04-20
aliases: []
tags: []
---
```

## Process Page

```yaml
---
type: process
status: active
created: 2026-04-20
updated: 2026-04-20
aliases: []
tags: []
---
```

## Project Page

```yaml
---
type: project
status: active
created: 2026-04-20
updated: 2026-04-20
aliases: []
tags: []
owner: Mario N
---
```

## Glossary Page

```yaml
---
type: glossary
status: active
created: 2026-04-20
updated: 2026-04-20
aliases: []
tags: []
---
```

## Map Page

```yaml
---
type: map
status: active
created: 2026-04-20
updated: 2026-04-20
aliases: []
tags: []
---
```

## Source Summary Page

```yaml
---
type: source-note
status: active
created: 2026-04-20
updated: 2026-04-20
aliases: []
tags: []
source_path: "01 - Raw Sources/_Inbox/source-file.md"
source_date: 2026-04-20
---
```

## Daily Note

```yaml
---
type: daily
date: 2026-04-20
---
```

## Workbench Note

```yaml
---
type: workbench
status: draft
created: 2026-04-20
updated: 2026-04-20
aliases: []
tags: []
---
```

---

## Rules for Agents

- always add frontmatter to long-term pages
- do not invent new `type` values without updating the schema
- keep dates in ISO format
- update `updated` on major page edits
- do not delete `created`
- add aliases only when there is a real search need
- keep tags short and few
- do not store secrets in frontmatter

---

## What to Avoid

Do not:
- mix many custom fields without reason
- turn frontmatter into a huge database
- add blank fields just to fill space
- use tags to replace clean links
- change type values page by page

The frontmatter should stay light and predictable.