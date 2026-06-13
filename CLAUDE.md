# Wellington AI — Master Context File
> Read this at the start of every session before doing any work.

## Company
Wellington AI Limited (UK entity). Founder & CEO: Raja Vasu. Contact: digitalhub559@gmail.com.
Building AI-powered intelligence platforms for workforce and trade sectors.

---

## Tool Portfolio

| Tool | Folder | Main File | Status |
|------|--------|-----------|--------|
| EmployAI | `employai/` | `employai/index.html` | Live — UK grant approved |
| TradeAI | `tradeai/` | `tradeai/index.html` | Live — UK grant approved |
| UrbanAI | `urbanai/` | `urbanai/index.html` | MVP complete — HMRC R&D report prepared |
| Tool 4 | TBD | TBD | Planning |

**Read each tool's `CONTEXT.md` before working on it.**

---

## Folder Structure

```
wellingtonAi/
├── CLAUDE.md                        ← this file (read every session)
├── index.html                       ← Wellington AI homepage
├── employai/
│   ├── CONTEXT.md                   ← EmployAI context (read before working on it)
│   ├── index.html                   ← EmployAI platform
│   └── ei-rubric.json               ← scoring rubric data
├── tradeai/
│   ├── CONTEXT.md                   ← TradeAI context (read before working on it)
│   ├── index.html                   ← TradeAI platform (~1,271 lines)
│   ├── TradeAI_Grant_Application.docx
│   ├── TradeAI_NSF_SBIR_Phase1_Application.docx
│   └── TradeAI_Q3_Supplementary_Response.docx
├── urbanai/
│   ├── CONTEXT.md                   ← UrbanAI context (read before working on it)
│   └── index.html                   ← UrbanAI platform (14 cities, 5 tabs, 30-yr financial model)
├── EI-Index/                        ← legacy EmployAI files (older version)
│   ├── employability-index.html
│   ├── ei-rubric.json
│   └── EmployAI_Grant_Application.docx
├── EmployAI_Q3_Supplementary_Response.docx
├── InnovateUK_Smart_Grant_Brief.docx
├── WellingtonAI_HMRC_Field_of_Technology.docx
└── WellingtonAI_HMRC_RD_Activities_Log.docx
```

---

## Shared Technical Conventions (apply to all tools)

- **Single-file HTML apps** — each tool is one self-contained `index.html`
- **No server dependency** — all computation runs client-side in the browser
- **Chart.js** — use `safeChart()` wrapper that destroys existing instance before creating new one (prevents duplicate canvas errors on tab/industry switch)
- **Navy colour** `#1F3864` — primary brand colour used across all tools and documents
- **Arial font** — all documents and UI elements
- **Docx generation** — Node.js `docx` npm package. `NODE_PATH=/usr/local/lib/node_modules_global/lib/node_modules`. Always validate with `python mnt/.claude/skills/docx/scripts/office/validate.py`
- **Table syntax in JS** — NEVER use inline `new TableRow({ children: [new TableCell({...})})]})` chains; always expand to multi-line with explicit `rows: [ new TableRow({ children: [ new TableCell({...}) ] }) ]` to avoid syntax errors

---

## Grant Status

### UK R&D Tax Credit (HMRC)
- Both EmployAI and TradeAI: **approved**
- Annual retrospective claim — no reapplication needed, continues each year
- HMRC now requires: (1) field of technology identification, (2) R&D activities log
- Key docs: `WellingtonAI_HMRC_Field_of_Technology.docx`, `WellingtonAI_HMRC_RD_Activities_Log.docx`
- Q3 competent professional challenge responded to for both platforms

### Innovate UK Smart Grant (UK)
- **Not yet applied** — next round monitoring required at ukri.org
- TradeAI recommended as first application; EmployAI to follow 6–12 months later
- Expected grant: £315K–£380K (single company), up to £650K with university partner
- Key doc: `InnovateUK_Smart_Grant_Brief.docx`
- Cash flow: spend-first, claim every 6 months; set up grant-backed loan facility

### NSF SBIR Phase I (US)
- **Requires US C-Corp first** (51% user / 49% Wellington AI India)
- Delaware C-Corp — estimated setup cost £8K–£11K with attorney
- Raja visa path: L-1A (new office, ~1-year initial period) → EB-1C green card (~2.5–3.5 years)
- NSF Phase I: $305K. Project Pitch opens June 2 2026. Current window likely missed — target next cycle early 2027
- Key doc: `tradeai/TradeAI_NSF_SBIR_Phase1_Application.docx`

---

## Working Protocol for New Sessions

1. Read `CLAUDE.md` (this file) — 1 minute
2. Read the specific tool's `CONTEXT.md` — 1 minute  
3. If editing code: read the relevant section of `index.html` before making changes
4. After significant changes: update the tool's `CONTEXT.md` with what changed
5. For new tools: write `CONTEXT.md` design brief **before** writing any code
