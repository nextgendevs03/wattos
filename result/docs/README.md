# WattOS — Generated Documents

This folder contains three client-ready documents for the WattOS portal quotation:

| Document | Description |
|----------|-------------|
| **01-Stakeholder-Analysis-Features-Pricing.md** | Features, screens, APIs, efforts, timeline, **total price ₹66,28,000**, phase-wise amounts, **project complexity (business view)**, cost justification (man-days & rates) |
| **02-Technical-Documentation-Architecture.md** | Architecture diagram, tech stack (Node + Python/AI), **project complexity (technical view)**, **technical challenges & resolution (latest tech)**, multi-language repo, cost justification, integrations, effort, API summary |
| **03-Phased-Launch-Pricing-Timeline.md** | Three phases with **₹20,12,000 \| ₹26,14,400 \| ₹20,01,600** and launch timeline |

---

## Export to PDF or Word

### Option 1: VS Code / Cursor (Markdown to PDF)

1. Install the **Markdown PDF** extension (e.g. "Markdown PDF" by yzane).
2. Open each `.md` file (01, 02, 03).
3. Right-click in the editor → **Markdown PDF: Export (pdf)** (or use Command Palette: `Markdown PDF: Export (pdf)`).
4. PDF will be generated in the same folder or a configured output folder.

### Option 2: Paste into Google Docs or Word

1. Open each `.md` file in a text editor.
2. Copy the full content.
3. Paste into **Google Docs** or **Microsoft Word**.
4. Adjust headings/tables if needed, then **File → Download → PDF** (Google Docs) or **Save As → PDF** (Word).

### Option 3: Pandoc (command line)

If you have [Pandoc](https://pandoc.org/) installed:

```bash
cd result/docs
pandoc 01-Stakeholder-Analysis-Features-Pricing.md -o 01-Stakeholder-Analysis-Features-Pricing.pdf
pandoc 02-Technical-Documentation-Architecture.md -o 02-Technical-Documentation-Architecture.pdf
pandoc 03-Phased-Launch-Pricing-Timeline.md -o 03-Phased-Launch-Pricing-Timeline.pdf
```

For Word (`.docx`):

```bash
pandoc 01-Stakeholder-Analysis-Features-Pricing.md -o 01-Stakeholder-Analysis-Features-Pricing.docx
pandoc 02-Technical-Documentation-Architecture.md -o 02-Technical-Documentation-Architecture.docx
pandoc 03-Phased-Launch-Pricing-Timeline.md -o 03-Phased-Launch-Pricing-Timeline.docx
```

### Option 4: md-to-pdf (Node.js)

```bash
npx md-to-pdf result/docs/01-Stakeholder-Analysis-Features-Pricing.md
npx md-to-pdf result/docs/02-Technical-Documentation-Architecture.md
npx md-to-pdf result/docs/03-Phased-Launch-Pricing-Timeline.md
```

*Note: Mermaid diagrams in Doc 2 may need a tool that supports Mermaid (e.g. VS Code Markdown PDF with mermaid support, or export the diagram separately from [mermaid.live](https://mermaid.live)).*
