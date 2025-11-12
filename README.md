# Flow Studio

**Version 0.0.1** — Universal Design Intelligence Engine

Flow Studio is a multi-style design engine that generates beautiful, accessible landing pages from natural language. Adaptable to any aesthetic—from premium medical to playful kids brands—while maintaining systematic quality and accessibility standards.

---

## 🎯 What Is Flow Studio?

Flow Studio transforms natural language intent into complete, production-ready landing pages through an intelligent agent workflow:

- **Arto** (UI/UX Strategist) → Creates layout structure and content hierarchy
- **Stylist** (Design Polish) → Generates design tokens with accessibility validation
- **Builder** (Components/HTML) → Produces semantic HTML/CSS with responsive design
- **Curator** (Evaluator) → Reviews output and suggests improvements

---

## ✨ Key Features

### Style-Agnostic Architecture
- **Universal token template** that adapts to any aesthetic
- Same layout structure generates different visual systems
- Examples: Minimal SaaS, Premium Medical, Luxury, Playful Kids

### Accessibility-First
- WCAG AAA compliance for body text (7:1 contrast)
- WCAG AA for interactive elements (4.5:1 contrast)
- Semantic HTML5, keyboard navigation, screen reader support

### Token-Based Design System
- Systematic approach to colors, typography, spacing
- 4px base spacing scale for visual consistency
- All design values as CSS custom properties

### No Dependencies
- Vanilla HTML/CSS (optional Tailwind CDN)
- No build tools required
- Works in any environment

---

## 📁 Repository Structure

```
Flow-Arto/
├── .claude/
│   ├── agents/                    # Agent definitions
│   │   ├── arto-ui-ux-strategist.md
│   │   ├── stylist-design-polish.md
│   │   ├── builder-components.md
│   │   └── curator-evaluator.md
│   └── BOOTSTRAP.md               # Quick start guide
├── design/
│   ├── layout.md                  # Layout structure (style-agnostic)
│   ├── tokens.json                # Token template (unpopulated)
│   └── tokens.minimal-saas.json   # Minimal SaaS tokens (v0.0.1)
├── docs/
│   └── DESIGN-ENGINE.md           # Design system foundation
├── web/
│   └── mock/
│       ├── index.html             # Generated HTML
│       └── styles.css             # Generated CSS
├── FLOW_STUDIO_SPEC.md            # Master specification
└── README.md                      # This file
```

---

## 🚀 Quick Start

### 1. Review the Specification
Read `FLOW_STUDIO_SPEC.md` for the complete system overview.

### 2. Explore Design Engine
Check `docs/DESIGN-ENGINE.md` for token system and design principles.

### 3. View Example Output
Open `web/mock/index.html` in a browser to see the Minimal SaaS implementation.

### 4. Review Design Tokens
- **Template:** `design/tokens.json` (style-agnostic schema)
- **Concrete Example:** `design/tokens.minimal-saas.json`

---

## 🎨 Creating New Design Systems

To create a new aesthetic (e.g., "luxury"):

1. **Derive from template:**
   ```bash
   cp design/tokens.json design/tokens.luxury.json
   ```

2. **Populate placeholders:**
   - Replace `<PRIMARY_BRAND_COLOR>` with `#1A1A1A` (black)
   - Replace `<ACCENT_BRAND_COLOR>` with `#D4AF37` (gold)
   - Fill all other tokens following examples in template

3. **Validate accessibility:**
   - Ensure contrast ratios meet WCAG standards
   - Document validation in `_accessibility` section

4. **Generate HTML/CSS:**
   - Builder reads `layout.md` + `tokens.luxury.json`
   - Produces new visual output with same structure

---

## 📊 Version 0.0.1 Milestone

### Achievements
✅ Complete agent workflow implemented (Arto → Stylist → Builder → Curator)
✅ Style-agnostic token template created
✅ First end-to-end test successful (Minimal SaaS)
✅ Production-ready HTML/CSS generated (9.6/10 Curator score)
✅ WCAG AAA accessibility compliance

### Metrics
- **1,223 lines** of code generated (tokens + HTML + CSS)
- **8 sections** implemented from layout specification
- **100% semantic HTML5** with proper accessibility
- **12.63:1 contrast** for body text (exceeds WCAG AAA)

---

## 🛠️ Technical Stack

- **HTML5** — Semantic markup
- **CSS3** — Custom properties (CSS variables)
- **Design Tokens** — JSON format
- **Fonts** — Google Fonts (Inter for Minimal SaaS)
- **No JavaScript** — Static prototype

---

## 📚 Documentation

- **`FLOW_STUDIO_SPEC.md`** — Master specification
- **`docs/DESIGN-ENGINE.md`** — Design system foundation
- **`.claude/BOOTSTRAP.md`** — Workflow and quick start
- **`.claude/agents/*.md`** — Individual agent definitions
- **`design/layout.md`** — Layout structure (style-agnostic)

---

## 🎯 Roadmap

### Planned (Future Versions)
- Additional aesthetic examples (Luxury, Playful Kids, Premium Medical)
- Dark mode token variants
- Extended component library (tables, tabs, accordions)
- Animation pattern library
- Automated accessibility testing integration

---

## 🧪 Testing

### End-to-End Test (v0.0.1)
- **Input:** "Minimal Premium SaaS" aesthetic description
- **Process:** Template → Tokens → HTML/CSS
- **Output:** Complete landing page (304 lines HTML, 727 lines CSS)
- **Quality:** 9.6/10 (Curator evaluation)

### Accessibility Validation
- Body text: 12.63:1 contrast (WCAG AAA ✓)
- Buttons: 4.82:1 contrast (WCAG AA ✓)
- Touch targets: 48px (exceeds 44px minimum ✓)

---

## 📄 License

[To be determined]

---

## 🙏 Acknowledgments

Built with Claude Code Web — demonstrating AI-powered design composition with systematic quality standards.

---

**Flow Studio v0.0.1** — Any Design System, Generated Naturally
