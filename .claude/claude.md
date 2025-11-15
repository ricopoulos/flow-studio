# Flow Studio - Claude Session Context

## Repository Identity

**Important: This repository was renamed from "Flow-Arto" to "flow-studio" on 2025-11-13**

### What is Flow Studio?

**Flow Studio** is an intelligent design tool/platform being developed to create systematic, brand-aware web projects using AI design agents.

- **Repository Purpose**: Development workspace for Flow Studio and all projects built with it
- **Main Page Purpose**: Production landing page with 8-theme showcase + project examples
- **Target Use**: Build client projects with systematic design approach + demonstrate design system capabilities

### Design Philosophy

Flow Studio uses specialized AI agents working from brand configs and design tokens:
- **Arto**: UX Strategist (layout & hierarchy)
- **Stylist**: Design tokens & visual coherence
- **Builder**: Semantic HTML & component implementation
- **Curator**: QA, accessibility, brand alignment
- **Maestro**: Workflow orchestration

---

## Repository Structure

```
flow-studio/                              (renamed from Flow-Arto)
├── index.html                            ← Main landing page (8-theme system)
├── styles.css                            ← Theme-aware CSS system
├── themes.js                             ← 8 design theme definitions
├── .nojekyll                             ← GitHub Pages config (bypass Jekyll)
├── docs/
│   └── PREVIEW.md                        ← Live URL documentation
├── design/
│   └── tokens.flow-studio.json           ← Design tokens for Flow Studio brand
├── brands/                               ← Brand configs for different projects
├── components/                           ← Reusable component specs
├── curator/                              ← QA and evaluation tools
└── web/                                  ← Live project outputs
    ├── flow-studio/                      ← Legacy location (8-theme system now at root)
    │   ├── index.html
    │   ├── styles.css
    │   └── themes.js
    └── carlton-select/                   ← Example client project (luxury hotel)
        └── index.html
```

---

## GitHub Pages URLs (After Consolidation)

**Base URL**: `https://ricopoulos.github.io/flow-studio/`

### Live Pages
- **Main Landing (8-Theme Showcase)**: `https://ricopoulos.github.io/flow-studio/`
- **Carlton Select Example**: `https://ricopoulos.github.io/flow-studio/web/carlton-select/`

### Legacy URLs (Redundant but still functional)
- **Old Flow Studio Path**: `https://ricopoulos.github.io/flow-studio/web/flow-studio/`

### URL Pattern for Future Projects
`https://ricopoulos.github.io/flow-studio/web/<project-slug>/`

---

## Current Development Status (as of 2025-11-15)

### ✅ Major Milestone: 8-Theme System Complete

**What We Built:**
1. **8 Interactive Design Variations** - Live theme switching system demonstrating 2025 web design trends:
   - **Token Pure** (default) - Design token system showcase
   - **Scroll Master** - Parallax & scroll-triggered animations
   - **Micro Magic** - Micro-animations & smart interactions
   - **3D Depth** - Floating UI & depth effects
   - **Type Hero** - Bold, kinetic typography
   - **Grid Artist** - Asymmetric layouts & CSS Grid
   - **Motion Flow** - Smooth animations & spring physics
   - **Dark Vivid** - High-contrast dark mode

2. **Technical Implementation:**
   - CSS variable-based theming (instant theme switching)
   - `themes.js` with 8 complete design token sets
   - Theme switcher UI with floating 🎨 button
   - localStorage persistence for user preference
   - Scroll-reveal animations using Intersection Observer
   - Full accessibility (keyboard nav, ARIA, reduced-motion)
   - Responsive across all 8 themes

3. **Consolidated Landing Page:**
   - Moved 8-theme system from `/web/flow-studio/` to root `/`
   - Added "Showcase" section featuring example projects
   - Single cohesive experience at main URL
   - Meta-demonstration: the page itself proves Flow Studio's multi-theme capability

### ✅ Previously Completed

1. **Flow Studio Landing Page Foundation** (original at `/web/flow-studio/`)
   - Token-driven design system (100% CSS variables)
   - WCAG AAA accessibility (all contrasts 7:1+)
   - Semantic HTML with proper ARIA
   - Fully responsive (375px → desktop)

2. **Carlton Select** (`/web/carlton-select/`)
   - Luxury hotel micro-landing page
   - Navy, gold, champagne palette
   - Linked from main landing showcase section

3. **Design Token System**
   - `design/tokens.flow-studio.json` fully documented
   - Colors, typography, spacing, shadows, motion
   - All contrast ratios validated (WCAG AAA)

---

## The 8-Theme System Explained

### Core Architecture

**CSS Variables as Theme Interface:**
```css
:root {
  /* Dynamic theme variables (updated by JavaScript) */
  --color-primary: #475569;
  --color-accent: #2563eb;
  --font-heading: 'Inter', sans-serif;
  --spacing-section: 96px;
  --motion-duration: 0.25s;
  --gradient-hero: linear-gradient(...);
  /* ... etc */
}
```

**Theme Switching:**
- User clicks 🎨 button → theme selector opens
- Click theme → JavaScript updates CSS variables
- Entire page re-themes instantly (no reload)
- Preference saved to localStorage

**Why This Matters:**
- **Proof of concept**: Shows Flow Studio can generate multiple coherent brand variations
- **Client demonstration**: Clients can experience different aesthetics live
- **Design intelligence**: Each theme is a complete, systematic design system
- **2025-ready**: Demonstrates modern web capabilities (CSS Grid, custom properties, animations)

---

## Working with Claude on This Project

### Key Principles
1. **Token-driven everything**: No hardcoded colors, spacing, or typography
2. **Accessibility first**: WCAG AAA contrast (7:1+), semantic HTML, keyboard nav
3. **Systematic approach**: Every design decision traceable to tokens/brand config
4. **Theme consistency**: Each theme must be complete and coherent across all elements
5. **Documentation**: Keep PREVIEW.md and claude.md current

### Typical Workflow (Updated for Multi-Theme)
1. Define/update brand config (in `/brands/`)
2. Generate/refine tokens (in `/design/`)
3. Create theme variations (in `themes.js`)
4. Build project with theme-aware CSS (CSS variables)
5. Test all theme variations for consistency
6. Run Curator QA on each theme
7. Update documentation
8. Merge to main for GitHub Pages deployment

### Important Files to Know
- **themes.js**: 8 theme definitions with complete token sets
- **styles.css**: Theme-aware CSS using CSS variables
- **index.html**: Main landing page with theme switcher
- **PREVIEW.md**: Canonical source for all live URLs
- **tokens.flow-studio.json**: Complete design token system
- **FLOW_STUDIO_SPEC.md**: Original platform specification
- **claude.md** (this file): Session context and history

---

## Recent Major Changes (Session 2025-11-15)

### 8-Theme System Implementation ✅
**Date**: 2025-11-15
**Scope**: Complete redesign and enhancement

**Research Phase:**
- Investigated 2025 web design trends (scroll effects, micro-animations, 3D, bold typography)
- Researched modern front-end tech (CSS Grid, Framer Motion, AOS, design tokens)
- Compiled 8 key trends for landing pages

**Design Phase:**
- Created 8 distinct aesthetic directions, each with:
  - Complete color palette (10 colors each)
  - Typography system (font families, weights, sizes)
  - Spacing and motion characteristics
  - Unique visual identity and purpose

**Technical Implementation:**
- Built `themes.js` with 8 theme objects
- Rebuilt `styles.css` as theme-aware system
- Created theme switcher UI component
- Added scroll-reveal animations
- Implemented localStorage persistence
- Full responsive support across all themes

**Consolidation:**
- Moved 8-theme system from `/web/flow-studio/` to root
- Created "Showcase" section featuring projects
- Single unified landing page experience
- Improved first impression and brand impact

**Results:**
- ✅ 8 fully functional, coherent design variations
- ✅ Instant theme switching (no page reload)
- ✅ All themes responsive and accessible
- ✅ META proof-of-concept: the page demonstrates Flow Studio's capability

### GitHub Pages Configuration Fix ✅
**Issue**: Subdirectories returning 404 (Jekyll processing paths)
**Fix**: Added `.nojekyll` file to bypass Jekyll
**Result**: All URLs working correctly

---

## Next Development Phase: Multi-Theme Sub-Projects

### Vision
Apply the 8-theme system to sub-projects (Carlton Select, future projects) so each example project can showcase multiple design variations.

### Technical Approach
1. Extract theme system into shared resources (`/shared/themes.js`, `/shared/theme-styles.css`)
2. Update sub-projects to import shared theme system
3. Create project-specific theme overrides where needed
4. Ensure theme switcher works consistently across all projects
5. Document theme application guide for new projects

### Benefits
- **Consistency**: Same 8 themes available across all Flow Studio projects
- **Client Value**: Show clients multiple design options for their project
- **Demonstration**: Prove systematic design approach scales across projects
- **Efficiency**: Reusable theme infrastructure

### Status
**Planning phase** - to be implemented in next session

---

## Development Branch Pattern

All development should happen on branches following this pattern:
- Branch name: `claude/<description>-<sessionId>`
- Example: `claude/consolidate-landing-01WrBqEZn4371QwZHyFE3s2S`
- Push to feature branch, then create PR to merge to main
- Main branch deploys to GitHub Pages automatically

**GitHub Pages Source:**
- Must be set to: **Branch: main / (root)**
- Check: Settings → Pages → Source

---

## Session Notes & Learnings

### GitHub Pages Gotchas
1. **Jekyll Processing**: By default, GH Pages uses Jekyll which can block certain paths
   - **Fix**: Add `.nojekyll` file at root
2. **Build Time**: 2-5 minutes after merge for deployment
3. **Cache Issues**: Use hard refresh (Ctrl+Shift+R) or incognito to see changes
4. **Protected Main**: Can't push directly to main - requires PR workflow

### Theme System Architecture Decisions
1. **CSS Variables vs. Classes**: Chose CSS variables for instant switching without class manipulation
2. **JavaScript Minimal**: Keep JS light - only theme switching and scroll reveals
3. **localStorage**: Persist theme preference for better UX
4. **Accessibility**: Each theme must pass WCAG AAA independently

### Design System Evolution
- Started: Single token set for Flow Studio brand
- Now: 8 complete theme variations, each internally consistent
- Next: Shared theme system for sub-projects

---

**Last Updated**: 2025-11-15
**Status**: 8-theme system live at root URL, ready for sub-project expansion
