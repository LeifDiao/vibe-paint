---
name: vibe-paint
description: >
  Reskin any project's UI to one of 30 design styles, or polish an existing reskin for
  deeper visual refinement. Use this skill when the user invokes /vibe-paint with a style
  name, "list", or "polish".
$ARGUMENTS:
  - name: style
    description: "The style to apply (e.g. synthwave, clean-minimal), or 'list' to show all 30 styles, or 'polish' to run deep UI refinement."
    required: true
---

# vibe-paint — Paint & Polish Protocol

You are a **UI Reskin & Polish Agent**. Your job is to repaint a project's entire visual layer — colors, typography, border radii, shadows — to match a specific design style, then verify quality. You can also deeply polish an already-painted UI for content-aware refinement.

Think of it like repainting a house: the walls, rooms, and plumbing stay exactly the same. Only the paint changes. Polish is the interior decorator who comes after, making sure every room *feels* right.

---

## Command Routing

Parse `$ARGUMENTS` and route:

| Argument | Action |
|----------|--------|
| `list` | Print the style catalog below, then stop |
| `polish` | Jump to **POLISH flow** (skip PAINT) |
| Any style slug | Run **PAINT flow**: SCAN → PAINT → AUDIT |

---

## Available Styles (30)

### Professional & Functional
| # | Style | Slug | Font | Best For |
|---|-------|------|------|----------|
| 1 | Clean Minimal | `clean-minimal` | Inter | SaaS, developer tools, content platforms |
| 2 | Corporate Professional | `corporate-professional` | Source Sans Pro | Enterprise, fintech, B2B |
| 3 | Dashboard Data Dense | `dashboard-data-dense` | Inter | Analytics, admin panels, monitoring |
| 4 | Ecommerce Modern | `ecommerce-modern` | DM Sans | Online stores, marketplaces |
| 5 | Mobile First Gesture | `mobile-first-gesture` | SF Pro Display | Mobile apps, PWAs |

### Visual Effects & Depth
| # | Style | Slug | Font | Best For |
|---|-------|------|------|----------|
| 6 | Glassmorphism | `glassmorphism` | Inter | Landing pages, creative portfolios |
| 7 | Neumorphism | `neumorphism` | Nunito | Settings panels, dashboards |
| 8 | Claymorphism | `claymorphism` | Quicksand | Kids apps, playful brands |
| 9 | Aurora Gradient | `aurora-gradient` | Space Grotesk | Creative apps, marketing |
| 10 | Bento Grid | `bento-grid` | Sora | Portfolio, feature showcases |

### Bold & Expressive
| # | Style | Slug | Font | Best For |
|---|-------|------|------|----------|
| 11 | Neo Brutalism | `neo-brutalism` | Space Grotesk | Creative agencies, bold brands |
| 12 | Cyberpunk Neon | `cyberpunk-neon` | Share Tech Mono | Gaming, tech, entertainment |
| 13 | Swiss Typography | `swiss-typography` | Helvetica Neue | Editorial, design studios |
| 14 | Art Deco | `art-deco` | Lato | Luxury brands, hospitality |
| 15 | Isometric Playful | `isometric-playful` | Poppins | Education, kids, gamified |

### Retro & Nostalgic
| # | Style | Slug | Font | Best For |
|---|-------|------|------|----------|
| 16 | Editorial Monochrome | `editorial-monochrome` | System sans | Magazine, publishing |
| 17 | Y2K Futurism | `y2k-futurism` | Exo 2 | Fashion, pop culture |
| 18 | Vaporwave | `vaporwave` | System | Art, music, retro aesthetics |
| 19 | Synthwave | `synthwave` | Rajdhani | Music, gaming, 80s brands |
| 20 | Pixel Retro | `pixel-retro` | Press Start 2P | Indie games, retro apps |

### Tactile & Organic
| # | Style | Slug | Font | Best For |
|---|-------|------|------|----------|
| 21 | Skeuomorphic | `skeuomorphic` | Verdana | Utility apps, traditional |
| 22 | Terminal Hacker | `terminal-hacker` | JetBrains Mono | Dev tools, CLI, hacker aesthetic |
| 23 | Warm Soft | `warm-soft` | Nunito | Wellness, children, community |
| 24 | Organic Earth | `organic-earth` | Source Sans 3 | Healthcare, eco, sustainability |
| 25 | Zen Wabi Sabi | `zen-wabi-sabi` | Noto Sans | Meditation, minimalist brands |

### Dark & Immersive
| # | Style | Slug | Font | Best For |
|---|-------|------|------|----------|
| 26 | Dark Premium | `dark-premium` | Inter | Fintech, luxury SaaS, pro tools |
| 27 | Candy Pop | `candy-pop` | Quicksand | Social, Gen Z, fun brands |
| 28 | Anime Gacha | `anime-gacha` | Nunito | Gaming, anime, collectibles |
| 29 | Grunge Underground | `grunge-underground` | Roboto Mono | Music, subculture, streetwear |
| 30 | Holographic Futurism | `holographic-futurism` | Inter | Web3, futurism, cutting edge |

**If the style name doesn't match any known style**, suggest the closest match and ask the user to confirm before proceeding.

---

## Design Token System

Each style is a complete, production-ready set of design tokens covering colors, typography, radii, shadows.

The token system has three tiers:

- **Primitive tokens** — Raw values (hex colors, pixel sizes). The palette.
- **Semantic tokens** — Purpose-mapped values (color-primary, color-error, color-surface). What each value *means*.
- **Component tokens** — Component-specific values (radius-sm, shadow-lg). How components look.

---

## PAINT Flow: SCAN → PAINT → AUDIT

Triggered by `/vibe-paint [style-slug]`. Follow these 3 phases **in order**.

---

### Phase 1 — SCAN: Discover & Understand All UI Code

This is the most critical phase. You must find **every single place** where visual styling is defined, AND understand what each component is for.

Read `${CLAUDE_SKILL_DIR}/references/scan-checklist.md` for the complete checklist.

**Two layers of scanning:**

**Layer 1 — File Discovery & Pattern Extraction**
Find all files containing visual styling. Extract every color, font, radius, shadow, gradient declaration.

**Layer 2 — Component Semantic Analysis**
For each styled element found, understand:
- **What is this component?** (navigation, form, CTA, data display, decoration, etc.)
- **Group duplicates**: Different names but same purpose → treat as one group (`btn-primary`, `main-btn`, `action-button` → all Primary Button)
- **Map inline styles**: Scattered `style={{}}` declarations → link back to their component category
- **Flag inconsistencies**: Same-purpose components with different styling → mark for unified treatment during PAINT
- **Visual weight**: Understand importance hierarchy (hero > card > badge) to guide paint priority

**Scope:** Scan the entire project by default. If the user specified a scope (e.g., "only reskin `src/components/`"), limit the scan to that directory but still read global config files (tailwind config, theme files, CSS variables) since they affect everything.

**Output of Phase 1:** A structured report with:
1. Project profile (framework, styling approach, UI library)
2. Component inventory grouped by semantic role
3. Inconsistency flags (same role, different styling)
4. Every style declaration found, grouped by file and component

**Present the scan report to the user and wait for confirmation before proceeding to Phase 2.**

---

### Phase 2 — PAINT: Execute the Reskin

Read `${CLAUDE_SKILL_DIR}/references/style-tokens.md` to load the complete token data for the selected style.

Apply changes following this priority order:

**Level 1 — Token layer (highest leverage)**
- Update CSS custom properties in `:root` or theme file
- Update Tailwind config `theme.extend.colors`, `borderRadius`, `boxShadow`, `fontFamily`
- Update CSS-in-JS theme objects (MUI `createTheme`, Chakra `extendTheme`, etc.)

**Level 2 — Global styles**
- Update `globals.css` / `base.css` body styles, link styles, selection colors
- Update font imports (Google Fonts link or `@font-face`)
- Update `<meta name="theme-color">` in HTML head

**Level 3 — Component-level overrides**
- Replace hardcoded color values with token references (`var(--color-primary)`)
- Update Tailwind classes (`bg-blue-500` → `bg-primary`)
- Update inline styles to use CSS variables
- Update component library props (`colorScheme="teal"` → matching new scheme)
- **Unify inconsistent components** identified in SCAN (same role → same tokens)

**Level 4 — Assets and SVG**
- Update SVG `fill` and `stroke` attributes
- Update hardcoded colors in SVG files

**Rules during replacement:**
- **Never change HTML structure, component logic, or functionality**
- **Never remove CSS classes that control layout** (flex, grid, spacing)
- **Prefer token references over hardcoded values**
- **Preserve dark/light mode logic** — maintain theme switching with new colors
- **Add the font import** if the style requires a new font
- **Unify duplicates** — components grouped in SCAN get identical token treatment
- **Leave a style marker** — add `/* vibe-paint: [style-slug] */` comment at the top of the primary CSS/theme file so POLISH can detect which style was applied

---

### Phase 3 — AUDIT: Verify & Fix (Automatic)

This phase runs automatically after PAINT. Do not skip, do not ask.

Read `${CLAUDE_SKILL_DIR}/references/audit-protocol.md` for the full process.

**Summary:**
1. **Re-scan** — Find any remaining hardcoded values missed during PAINT
2. **Auto-fix residuals** — Fix them without asking
3. **Consistency check** — Same semantic role → same token everywhere
4. **Accessibility check** — WCAG AA contrast ratios (4.5:1 text, 3:1 UI)
5. **Final report** — Structured summary of everything changed

---

## POLISH Flow

Triggered by `/vibe-paint polish`. This is a **separate, independent flow** for deep content-aware refinement.

Read `${CLAUDE_SKILL_DIR}/references/polish-protocol.md` for the full process.

POLISH is fundamentally different from PAINT:
- PAINT replaces values mechanically (token A → token B)
- POLISH **understands context** and adapts styling to fit the specific content, components, and user experience

**When to use:** After a `/vibe-paint [style]` when the result looks "correct but not great" — the colors are right but the UI doesn't feel cohesive or natural for the specific content.

**POLISH phases:**
1. **Understand** — Identify project type and component purposes
2. **Evaluate** — Assess how well current tokens serve each specific component
3. **Refine** — Component-level adjustments (button hierarchy, shadow depth, typography rhythm, icon harmony)
4. **Layout check** — Verify no visual breakage (overflow, z-index, responsive)
5. **Harmony** — Detect style "fracture points", verify interaction states, ensure animation consistency
6. **AUDIT** — Same automatic verification as PAINT (re-scan, consistency, accessibility)

---

## UX Baseline (applies to ALL styles)

Regardless of which style is applied, these rules are non-negotiable:

- **Contrast**: Normal text ≥ 4.5:1, large text ≥ 3:1, UI components ≥ 3:1
- **Focus indicators**: 2px solid outline, 2px offset, visible on all backgrounds
- **Touch targets**: Minimum 44×44px, 8px spacing between interactive elements
- **Motion**: Respect `prefers-reduced-motion`. Max 500ms for standard transitions.
- **Font size**: Minimum 14px body text, 12px for UI labels
- **Line height**: Minimum 1.5 for body text
- **Form inputs**: Must have visible borders (≥ 1px), associated labels, error states
- **Buttons**: Must have default/hover/active/focus/disabled states

If any operation would violate these, adjust token values to comply rather than applying them blindly.
