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
index.md                             â† site homepage
index.md                          â† master index and query guide
format-spec.md                       â† Word and Figma output spec
global-guidelines.md              â† voice, tone, words to avoid
buttons.md â€¦ wizards.md        â† component sections
```

Each section follows: **When to use â†’ Style â†’ Behavior â†’ Do/Don't**

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

**Source Word document:** `Actian_Content_Guidelines_Claude3.docx` (maintainer's local copy â€” not committed to this repo)
