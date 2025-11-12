# Flow Studio – Natural-Language Design Composer (Web-First Spec)

## 🎯 Purpose
Create an intelligent **Flow orchestration for design**, capable of turning natural language intent into elegant, accessible landing page concepts.  
Run entirely in **Claude Code Web** — no local installs, no build tools.

---

## 🧩 Outcomes
By the end of the flow, the system should generate:

- A **Design Brief** summarizing goals, tone, and target audience.
- A **Layout Map** (`design/layout.md`) with structure, sections, and copy skeleton.
- A **Style Token file** (`design/tokens.json`) defining color palette, typography, spacing, shadows, and radii.
- A **Working HTML/CSS Mock** (`web/mock/index.html`, `web/mock/styles.css`) that is responsive, readable, and elegant.
- A **Rationale Summary** (`design/rationale.md`) explaining design choices and next-step suggestions.

---

## 🌐 Constraints for Claude Code Web
- **No CLI or dependency installs** unless explicitly approved.
- Prefer **vanilla HTML/CSS** or **Tailwind CDN**.
- **Playwright MCP** is available and optional:
  - Allowed tools: `browser_navigate`, `browser_take_screenshot`, `browser_console_messages`
  - Screenshot policy: JPEG, quality ≈ 60, max 1200×800, ≤3 per mission. Save file path only, don’t inline.
- Always show diffs before overwriting files.
- Ask before large refactors.

---

## 🗂️ Minimal Repository Structure (Claude should generate this)
/docs/STYLEGUIDE-UI.md               ← Brand design rules (seeded here)
/design/layout.md
/design/tokens.json
/design/rationale.md
/web/mock/index.html
/web/mock/styles.css
.claude/agents/arto-ui-ux-strategist.md
.claude/agents/stylist-design-polish.md
.claude/agents/builder-components.md
.claude/agents/curator-evaluator.md
.claude/BOOTSTRAP.md

---

## 🎨 Brand Seed (Design Context)
Elegant, premium-medical aesthetic with balanced whitespace and a trustworthy tone.

### Colors
| Role | Hex | Usage |
|------|------|--------|
| Primary | `#2B6CB0` | CTA / links |
| Neutral-900 | `#0A0A0A` | Headings |
| Neutral-700 | `#333333` | Body text |
| Surface | `#FFFFFF` | Background |
| Surface-Alt | `#F7FAFC` | Section alt background |
| Accent | `#B7791F` | Highlights |
| **Contrast** | Body ≥7:1, Buttons ≥4.5:1 |

### Typography
- Headings: `"Playfair Display", serif`
- Body: `"Inter", system-ui, sans-serif`
- Type scale: 32 / 24 / 20 / 16 / 14 px
- Line height: 1.35 (headings), 1.6 (body)

### Layout & Components
- Spacing base: 4px scale (8/12/16/24/32/48)
- Max width: 1024–1280px
- Buttons: 48px height, rounded corners, focus-visible, hover +6% brightness
- Cards: white, shadow-sm, radius-lg, 24px padding
- Forms: visible labels, accessible errors (`#B00020`), success states

---

## 🤖 Sub-Agents (Light Stubs to Generate)
- **Arto (UI/UX Strategist):** interprets intent → creates layout, flow, and content hierarchy. Reads `STYLEGUIDE-UI.md` first.  
- **Stylist (Design Polish):** improves color harmony, typography, rhythm, spacing. Outputs `design/tokens.json`.  
- **Builder (Components/HTML):** produces `web/mock/index.html` and `styles.css` (Tailwind CDN if desired). Enforces accessibility.  
- **Curator (Evaluator):** reviews all outputs, merges improvements, and writes `design/rationale.md`.

Each agent should have a short “How You Work” and a **Screenshot Policy** consistent with the limits above.

---

## 🧠 Working Sequence
1. **Plan:** Confirm goal, audience, and tone. Output short **Design Brief**.
2. **Arto:** Read `/docs/STYLEGUIDE-UI.md`, produce `design/layout.md` (structure, hierarchy, copy hooks).
3. **Stylist:** Generate `design/tokens.json` (palette, typography, spacing, shadows) with contrast validation.
4. **Builder:** Generate mock files in `/web/mock/` — ensure responsiveness and semantic HTML.
5. *(Optional)* **Browser QA:** Use Playwright MCP to capture 1 screenshot and collect console warnings.
6. **Curator:** Evaluate vs brief; merge best ideas; create `design/rationale.md`.
7. **Finalize:** Save diffs, document next steps (A/B testing ideas, visual assets, next goals).

---

## ✅ Deliverables Checklist
- `/docs/STYLEGUIDE-UI.md` — brand and tone foundation  
- `/design/layout.md`, `/design/tokens.json`, `/design/rationale.md`  
- `/web/mock/index.html`, `/web/mock/styles.css`  
- `.claude/BOOTSTRAP.md` — quick start and instructions

---

## 🧭 Review Gates (Stop & Ask)
- After **Arto layout**
- After **Stylist tokens**
- After **Builder mock**
- After **Curator rationale**

---

## 🚫 Non-Goals
- No heavy JS frameworks.
- No backend or API integration.
- No CI/CD for now — static prototype only.

---

## 🧩 First Action
Read this spec.  
Propose a **small, numbered plan** with exact filenames to be created.  
Wait for my approval before writing anything.

Once approved, execute **phase-by-phase**, showing diffs each time.

---

### 🪄 Claude Code Web startup prompt
After creating this file, open your repo in Claude Code Web and say:
> “Read `FLOW_STUDIO_SPEC.md`. Propose a small numbered plan and exact files you’ll create. Wait for approval before writing.”

