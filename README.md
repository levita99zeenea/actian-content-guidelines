---
title: "About"
nav_order: 40
---

# Actian Content Guidelines

UI writing standards for the Actian Data Intelligence platform. Source of truth for writers, designers, and product teams working on the knowledge catalog platform and associated products.

**Live site:** https://levita99zeenea.github.io/actian-content-guidelines

---

## Structure

37 section files, one per UI component or topic area, plus an index and format spec:

```
index.md                             ← site homepage
00-index.md                          ← master index and query guide
format-spec.md                       ← Word and Figma output spec
01-global-guidelines.md              ← voice, tone, words to avoid
02-buttons.md … 37-wizards.md        ← component sections
```

Each section follows: **When to use → Style → Behavior → Do/Don't**

---

## Editing guidelines

1. Edit the relevant section `.md` file directly on this repo
2. Changes publish to the live site automatically via GitHub Pages (allow ~1 min)
3. To sync changes to the Actian Design System plugin, update `plugins/actian-design-system/docs/content-guidelines.md` in the plugin repo and submit a PR

---

## Generating deliverables from these files

With the **Actian Design System Claude plugin** installed:

**Word document:**
```
/docx generate Actian content guidelines Word doc from content-guidelines/ directory using format-spec.md
```

**Figma presentation:**
```
/generate-presentation content guidelines from content-guidelines/ directory
```

---

## Style basis

All guidelines follow IBM Style conventions and are written in sentence case throughout.

**Source Word document:** `Actian_Content_Guidelines_Claude3.docx` (maintainer's local copy — not committed to this repo)
