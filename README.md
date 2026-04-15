# vibe-paint

[中文文档](./README_CN.md)

**Your app already works. Now make it *feel* different.**

![vibe-paint](docs/image.png)

vibe-paint is a Claude Code plugin that reskins your entire project's UI in one command. Pick a style, and it repaints every color, font, radius, and shadow across your codebase — then verifies the result for consistency and accessibility.

## Quick Start

```
# See all 30 styles
/vibe-paint list

# Reskin your project (replace with any style name)
/vibe-paint synthwave

# Deep content-aware refinement
/vibe-paint polish
```

## Installation

**Step 1** — Add the marketplace:

```
/plugin marketplace add LeifDiao/vibe-paint
```

**Step 2** — Install the plugin:

```
/plugin install vibe-paint@vibe-paint-marketplace
```

**Alternative (manual):**

```bash
git clone https://github.com/LeifDiao/vibe-paint.git ~/vibe-paint
claude --plugin-dir ~/vibe-paint
```

## The Problem This Solves

There are hundreds of UI libraries for *building* interfaces. Tailwind, MUI, Chakra, shadcn — they're all great when you're starting from scratch.

But what about the project you've already built?

Maybe you shipped a SaaS dashboard six months ago and now the brand is evolving. Maybe you're a solo dev who nailed the functionality but the visual layer feels generic. Maybe you just want to see what your app looks like in a completely different aesthetic — without spending a week manually hunting down every hex value, every `bg-blue-500`, every `border-radius: 8px` scattered across 40 files.

That's vibe-paint. One command. Entire project. New visual identity.

```
/vibe-paint synthwave
```

It scans your project, understands what each component is for, replaces every visual token with your chosen style, unifies inconsistencies it finds along the way, and audits the result for accessibility compliance. Then if you want to go further, `/vibe-paint polish` brings in context-aware refinement — adjusting button hierarchies, card depth, typography rhythm — because a mechanical token swap gets you 90% there, but the last 10% needs to understand *what your UI is actually showing*.

## How It's Different

| | UI Libraries (MUI, Chakra, Tailwind) | Design Tools (Figma, Framer) | **vibe-paint** |
|---|---|---|---|
| **When** | Before you build | Before you build | After you've built |
| **What** | Components to assemble | Mockups to hand off | Restyle what's already there |
| **Scope** | New projects | New designs | Existing codebases |
| **Output** | Code you write from scratch | Specs for devs to implement | Your code, repainted |

## Commands

| Command | What it does |
|---------|-------------|
| `/vibe-paint [style]` | Full reskin: SCAN → PAINT → AUDIT |
| `/vibe-paint list` | Show all 30 available styles |
| `/vibe-paint polish` | Deep content-aware UI refinement |

## How It Works

### Paint: swap the skin (`/vibe-paint synthwave`)

1. **SCAN** — Finds every style declaration in your project. But it doesn't just grep for hex values — it understands what each component *is*. Three buttons named `btn-primary`, `main-btn`, and `action-button`? Same thing. They'll get the same treatment.
2. **PAINT** — Replaces all visual tokens (colors, fonts, radii, shadows) with the selected style. Works across CSS variables, Tailwind configs, CSS-in-JS theme objects, inline styles, SVG attributes — whatever your project uses.
3. **AUDIT** — Automatic verification. Catches leftover hardcoded values hiding in `:hover` states and ternary expressions. Checks every color combination for WCAG AA contrast. Fixes what it finds without asking.

### Polish: refine the feel (`/vibe-paint polish`)

Paint gets the values right. Polish makes the *experience* right.

After a paint, your app has the correct colors and fonts — but a product card and a settings panel shouldn't have the same visual weight just because they're both "cards." Polish understands your content:

- **Understands** your project type (e-commerce, dashboard, blog, SaaS) and each component's purpose
- **Evaluates** whether the style tokens actually serve each component well — does synthwave's neon glow make sense on a form label?
- **Refines** button hierarchy, shadow depth, typography rhythm, interaction states
- **Checks** layout integrity — overflow, z-index, responsive behavior after the style change
- **Harmonizes** the whole UI — finds "fracture points" where the style suddenly breaks, unifies hover/focus/active states
- **Audits** everything one final time for consistency and accessibility

## 30 Styles, 6 Categories

### Professional & Functional
| Style | Slug | Best For |
|-------|------|----------|
| Clean Minimal | `clean-minimal` | SaaS, developer tools |
| Corporate Professional | `corporate-professional` | Enterprise, fintech |
| Dashboard Data Dense | `dashboard-data-dense` | Analytics, admin panels |
| Ecommerce Modern | `ecommerce-modern` | Online stores |
| Mobile First Gesture | `mobile-first-gesture` | Mobile apps, PWAs |

### Visual Effects & Depth
| Style | Slug | Best For |
|-------|------|----------|
| Glassmorphism | `glassmorphism` | Landing pages, portfolios |
| Neumorphism | `neumorphism` | Settings, dashboards |
| Claymorphism | `claymorphism` | Kids apps, playful brands |
| Aurora Gradient | `aurora-gradient` | Creative apps, marketing |
| Bento Grid | `bento-grid` | Portfolio, showcases |

### Bold & Expressive
| Style | Slug | Best For |
|-------|------|----------|
| Neo Brutalism | `neo-brutalism` | Creative agencies |
| Cyberpunk Neon | `cyberpunk-neon` | Gaming, tech |
| Swiss Typography | `swiss-typography` | Editorial, design studios |
| Art Deco | `art-deco` | Luxury brands |
| Isometric Playful | `isometric-playful` | Education, gamified |

### Retro & Nostalgic
| Style | Slug | Best For |
|-------|------|----------|
| Editorial Monochrome | `editorial-monochrome` | Magazine, publishing |
| Y2K Futurism | `y2k-futurism` | Fashion, pop culture |
| Vaporwave | `vaporwave` | Art, music |
| Synthwave | `synthwave` | Music, gaming |
| Pixel Retro | `pixel-retro` | Indie games |

### Tactile & Organic
| Style | Slug | Best For |
|-------|------|----------|
| Skeuomorphic | `skeuomorphic` | Utility apps |
| Terminal Hacker | `terminal-hacker` | Dev tools, CLI |
| Warm Soft | `warm-soft` | Wellness, community |
| Organic Earth | `organic-earth` | Healthcare, eco |
| Zen Wabi Sabi | `zen-wabi-sabi` | Meditation, minimalist |

### Dark & Immersive
| Style | Slug | Best For |
|-------|------|----------|
| Dark Premium | `dark-premium` | Fintech, luxury SaaS |
| Candy Pop | `candy-pop` | Social, Gen Z |
| Anime Gacha | `anime-gacha` | Gaming, anime |
| Grunge Underground | `grunge-underground` | Music, streetwear |
| Holographic Futurism | `holographic-futurism` | Web3, futurism |

## What It Handles

- CSS custom properties / variables
- Tailwind utility classes + config
- CSS-in-JS (styled-components, emotion, MUI themes, Chakra themes)
- Inline styles (React `style={{}}`, HTML `style=""`)
- Component library props (MUI, Chakra, Ant Design, shadcn/ui)
- SVG fill/stroke attributes
- Font imports and meta theme-color
- SCSS/Less/Stylus variables
- Gradient, shadow, and radius declarations

## License

MIT
