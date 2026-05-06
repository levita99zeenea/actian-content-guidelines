---
title: "Format spec"
nav_order: 39
---
# Content guidelines format spec

This file defines how content guideline markdown files should be formatted when generating deliverables — either as a consolidated Word document or as Figma presentation slides.

---

## Markdown source structure

Each section file follows this pattern:

```
# {N}. {Section title}

{One-sentence description of the component and its purpose}

---

## {N}.{M} {Subsection title}  ← only if section has subsections

### When to use  ← H3 subsection headers
### Style
### Behavior
### Do / Don't  ← always a table

| Do | Don't |
|---|---|
| ... | ... |
{: .do-dont-table}

### Examples  ← optional; always a table

| Element | Example text |
|---|---|
| ... | ... |
```

---

## Word document output

When generating a Word document from these files, use the following formatting rules:

### Page setup
- Paper: US Letter (8.5" × 11")
- Margins: 1" all sides
- Font: Arial throughout
- Base size: 11pt body, 18pt H1, 14pt H2, 12pt H3

### Heading styles
| Markdown | Word style | Notes |
|---|---|---|
| `# H1` | Heading 1 | Section title; page break before each H1 |
| `## H2` | Heading 2 | Subsection |
| `### H3` | Heading 3 | When/Style/Behavior labels |
| Bold text | Bold run | Keep inline |

### Tables
- Full-width (content width = 9,360 DXA for US Letter with 1" margins)
- Header row: light Actian blue fill (`#D5E8F0`), bold text
- Body rows: alternating white / light gray (`#F5F5F5`)
- All borders: light gray (`#CCCCCC`), 1pt
- Cell padding: 80/80/120/120 DXA (top/bottom/left/right)

### Do / Don't tables
- Two columns: "Do" (left, green tint `#E8F5E9`) and "Don't" (right, red tint `#FFEBEE`)
- Column widths: 4,680 DXA each

### Section dividers
- Horizontal rule (`---`) becomes a styled paragraph border, not a blank line

### Table of contents
- Auto-generated from H1 headings
- Hyperlinked

### Cover page
```
Actian Data Intelligence
Product and UI content guidelines
Version: {version}
Date: {date}
```

---

## Figma output

When generating Figma slides from these files:

### Slide structure
- One slide per H1 section (use `/generate-presentation` skill)
- Title slide: section number + title
- Content slides: one per H2 or major content block

### Component mapping
| Markdown element | Figma component |
|---|---|
| H1 title | Presentation / Section title frame |
| H2 heading | Presentation / Slide title |
| H3 heading | Presentation / Body heading |
| Paragraph | Presentation / Body text |
| Bullet list | Presentation / Bullet list |
| Do/Don't table | Presentation / Do-Don't comparison card |
| Example table | Presentation / Example table card |

### Color coding
- "Do" examples: green border `#4CAF50`
- "Don't" examples: red border `#F44336`
- Section header accent: Actian primary `var(--zen-color-theme-primary)`

---

## Generating outputs

### Word document
```
/docx generate content guidelines Word doc from content-guidelines/ directory
```
Claude will:
1. Read `00-index.md` to get section order
2. Concatenate all section files in order
3. Apply Word formatting per this spec
4. Save as `Actian_Content_Guidelines_{date}.docx` in the project directory

### Figma presentation
```
/generate-presentation content guidelines
```
Claude will:
1. Read each section file
2. Map content to Figma presentation components
3. Push slides to Figma via the MCP

### Querying guidelines
Ask the Actian Design System plugin directly:
- "What is the correct label for the back button in a stepper?"
- "How should empty states be written?"
- "What words should we avoid in UI copy?"
