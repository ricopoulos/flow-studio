# Flow Studio

**Intelligent design system platform with 8 live theme variations**

Flow Studio is a development platform using AI design agents to create systematic, brand-aware web projects. Built for designers and developers who value systematic design over magic templates.

🎨 **[View Live Demo](https://ricopoulos.github.io/flow-studio/)** - Experience all 8 design themes live!

---

## What is Flow Studio?

Flow Studio demonstrates a new approach to design systems: **multiple coherent brand variations from a single systematic foundation**. Our landing page itself is a META proof-of-concept—one page, 8 completely different design aesthetics, all token-driven.

### The 8 Design Variations

Click the 🎨 button on our landing page to experience:

1. **Token Pure** - Clean design token system showcase
2. **Scroll Master** - Parallax & scroll-triggered animations
3. **Micro Magic** - Micro-animations & smart interactions
4. **3D Depth** - Floating UI & depth effects
5. **Type Hero** - Bold, kinetic typography (96px headings!)
6. **Grid Artist** - Asymmetric layouts & CSS Grid
7. **Motion Flow** - Smooth animations & spring physics
8. **Dark Vivid** - High-contrast dark mode

Each theme is a complete design system with its own:
- Color palette (10 colors)
- Typography system (fonts, weights, scales)
- Spacing & motion characteristics
- Unique visual identity

**All powered by CSS variables. Switch instantly. No page reload.**

---

## The AI Agent System

Flow Studio uses specialized AI agents that work together:

- **Arto** - UX Strategist: Layout, hierarchy, information architecture
- **Stylist** - Design System: Generates design tokens from brand configs
- **Builder** - Implementation: Semantic HTML, accessible components
- **Curator** - QA: Brand alignment, accessibility, consistency checks
- **Maestro** - Orchestration: Coordinates workflow and refinement

### Philosophy

**Systematic, not magical.** Every design decision is traceable to a brand config or design token. No hardcoded values, no black-box generation, no "AI made this look weird and I don't know why."

---

## Repository Structure

```
flow-studio/
├── index.html                    # Main landing page (8-theme system)
├── styles.css                    # Theme-aware CSS (CSS variables)
├── themes.js                     # 8 theme definitions
├── .nojekyll                     # GitHub Pages config
├── docs/
│   └── PREVIEW.md               # Live URL documentation
├── design/
│   └── tokens.*.json            # Design token definitions
├── brands/
│   └── *.brand.json             # Brand configuration files
├── components/
│   └── *.component.json         # Reusable component specs
├── curator/
│   └── evaluation rules         # QA and validation
└── web/                         # Example projects
    ├── flow-studio/             # Legacy 8-theme location
    └── carlton-select/          # Luxury hotel example
```

---

## Live Examples

### Flow Studio Landing (8 Themes)
**URL**: https://ricopoulos.github.io/flow-studio/
**Features**:
- 8 interactive design variations
- Live theme switching (🎨 button)
- Scroll-reveal animations
- Project showcase section
- Fully responsive & accessible

### Carlton Select
**URL**: https://ricopoulos.github.io/flow-studio/web/carlton-select/
**Features**:
- Luxury hotel micro-landing page
- Navy/gold/champagne palette
- Premium aesthetic demonstration

---

## Technical Highlights

### Multi-Theme Architecture

**CSS Variables as Theme Interface:**
```css
:root {
  --color-primary: #475569;
  --color-accent: #2563eb;
  --font-heading: 'Inter', sans-serif;
  --spacing-section: 96px;
  --motion-duration: 0.25s;
  /* ... updated by theme switcher */
}
```

**Theme Switching Flow:**
1. User clicks 🎨 → theme selector opens
2. User selects theme → JavaScript updates CSS variables
3. Entire page re-themes instantly
4. Preference saved to localStorage

**Benefits:**
- No page reload required
- Smooth transitions
- Same HTML/structure, different visual identity
- Proof that systematic design scales

### Design Token System

Flow Studio projects are built from design tokens, not arbitrary CSS:

**`design/tokens.flow-studio.json`** defines:
- **Colors**: Primary, accent, neutral, semantic (all WCAG AAA validated)
- **Typography**: Font system, type scale, line heights, letter spacing
- **Spacing**: 4px base scale with component-specific values
- **Shadows**: Elevation system with focus states
- **Motion**: Duration and easing curves
- **Components**: Pre-defined button, input, card specs

All color pairings are validated for WCAG AAA contrast (7:1+).

---

## Quality Standards

### Token Usage
- ✅ All colors use CSS variables
- ✅ All spacing uses CSS variables
- ✅ All typography uses CSS variables
- ❌ No hardcoded hex values outside `:root`

### Accessibility (All 8 Themes)
- ✅ WCAG AAA contrast (7:1+) for all text
- ✅ Semantic HTML (`<header>`, `<main>`, `<nav>`, `<footer>`)
- ✅ ARIA labels where needed
- ✅ Keyboard navigation with visible focus states
- ✅ 44px minimum touch targets
- ✅ `prefers-reduced-motion` support

### Responsive Design
- ✅ Mobile-first approach (375px base)
- ✅ Tablet breakpoint (≥640px)
- ✅ Desktop breakpoint (≥1024px)
- ✅ No layout breaks at any width
- ✅ All 8 themes responsive

---

## Getting Started

### View the Demo

**Simply visit**: https://ricopoulos.github.io/flow-studio/

Click the 🎨 button to explore all 8 design variations. Try switching themes on different devices to see responsive behavior.

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/ricopoulos/flow-studio.git
   cd flow-studio
   ```

2. **Open locally**
   - Main landing: `index.html`
   - Example project: `web/carlton-select/index.html`

3. **Create a new project**
   ```bash
   mkdir web/new-project
   # Add index.html and styles.css
   ```

### Deployment

Projects deploy via **GitHub Pages** from the `main` branch:
- Merge to main → Automatic deployment
- Live at: `https://ricopoulos.github.io/flow-studio/`

**Important**: Ensure GitHub Pages is set to deploy from **Branch: main / (root)**

---

## Workflow

### Adding a New Project

1. **Define the brand** (in `/brands/<project>.brand.json`)
2. **Generate design tokens** (in `/design/tokens.<project>.json`)
3. **Build the project** (in `/web/<project-slug>/`)
   - Create `index.html`
   - Create `styles.css` (token-driven, theme-aware)
   - Optionally: Import shared theme system
4. **Run Curator QA**
   - Verify token usage (no hardcoded values)
   - Check accessibility (contrast, semantic HTML, ARIA)
   - Test responsive design
   - Test all theme variations
5. **Update showcase** (add to main landing page showcase section)
6. **Update docs** (`/docs/PREVIEW.md`) with live URL
7. **Merge to main** for deployment

---

## Future Development

### Next Phase: Multi-Theme Sub-Projects

**Vision**: Apply the 8-theme system to all sub-projects so each example can showcase multiple design variations.

**Approach**:
1. Extract theme system into shared resources
2. Update sub-projects to import shared themes
3. Create project-specific theme overrides
4. Consistent theme switcher across all projects

**Benefits**:
- Show clients multiple options for their project
- Prove systematic design scales
- Reusable theme infrastructure

---

## Documentation

- **[.claude/claude.md](.claude/claude.md)**: Complete session context and development history
- **[PREVIEW.md](docs/PREVIEW.md)**: Canonical source for all live URLs
- **[FLOW_STUDIO_SPEC.md](FLOW_STUDIO_SPEC.md)**: Original platform specification

---

## Tech Stack

- **HTML5**: Semantic, accessible markup
- **CSS3**: Token-driven design system with CSS variables
- **JavaScript**: Minimal (theme switching, scroll reveals)
- **Fonts**: Google Fonts (Inter, Sora, Space Grotesk)
- **Hosting**: GitHub Pages
- **Deployment**: Automatic from main branch

---

## Development Principles

1. **Systematic over magical**: Every decision traceable to config/tokens
2. **Token-driven**: No hardcoded values
3. **Accessibility first**: WCAG AAA by default
4. **Multi-theme capable**: Design for variation from the start
5. **Performance**: Minimal dependencies, fast load times
6. **Maintainable**: Clear structure, documented decisions
7. **Iterative**: Curator feedback → refinement loop

---

## Key Achievements

✅ **8-Theme System** - Multiple coherent design variations from one foundation
✅ **Instant Theme Switching** - CSS variable-based, no page reload
✅ **WCAG AAA Accessibility** - All themes, all elements
✅ **Fully Responsive** - Mobile-first, works across all devices
✅ **Systematic Design** - Every value traceable to design tokens
✅ **META Proof-of-Concept** - The landing page demonstrates its own capability

---

## License

Private development project. Not yet open source.

---

## Contact

For questions or collaboration opportunities, please reach out via GitHub.

---

**Built with systematic design, not magic.**
**Experience all 8 themes live: [ricopoulos.github.io/flow-studio](https://ricopoulos.github.io/flow-studio/)**
