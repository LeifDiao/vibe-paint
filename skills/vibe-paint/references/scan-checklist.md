# UI Scan Checklist

This document covers two layers of scanning: **Pattern Extraction** (finding every style declaration) and **Semantic Analysis** (understanding what each component is and grouping duplicates).

## Table of Contents
1. [File Discovery](#file-discovery)
2. [Config File Analysis](#config-file-analysis)
3. [Component Semantic Analysis](#component-semantic-analysis)
4. [CSS & Preprocessor Patterns](#css--preprocessor-patterns)
5. [Tailwind Patterns](#tailwind-patterns)
6. [CSS-in-JS Patterns](#css-in-js-patterns)
7. [Inline Style Patterns](#inline-style-patterns)
8. [Component Prop Patterns](#component-prop-patterns)
9. [SVG & Asset Patterns](#svg--asset-patterns)
10. [HTML Patterns](#html-patterns)
11. [Regex Reference](#regex-reference)

---

## File Discovery

Start by finding all files that could contain visual styling. Use these glob patterns:

```
# CSS and preprocessors
**/*.css
**/*.scss
**/*.sass
**/*.less
**/*.styl
**/*.stylus

# JavaScript/TypeScript (may contain CSS-in-JS, inline styles, Tailwind classes)
**/*.js
**/*.jsx
**/*.ts
**/*.tsx
**/*.mjs
**/*.cjs

# Vue single-file components (contain <style> blocks)
**/*.vue

# Svelte components (contain <style> blocks)
**/*.svelte

# HTML files
**/*.html
**/*.htm
**/*.ejs
**/*.hbs
**/*.pug
**/*.njk

# Config files (contain theme definitions)
tailwind.config.*
postcss.config.*
theme.js
theme.ts
theme.config.*
**/theme/**
**/tokens/**

# SVG assets
**/*.svg
```

Exclude these directories: `node_modules/`, `dist/`, `build/`, `.next/`, `.nuxt/`, `.svelte-kit/`, `coverage/`, `.git/`.

---

## Config File Analysis

Before scanning individual files, understand the project's architecture:

### package.json
Read `package.json` dependencies to identify:
- **Framework**: react, vue, svelte, angular, next, nuxt, gatsby, remix, astro
- **Styling**: tailwindcss, @emotion/react, styled-components, @stitches/react, vanilla-extract, @vanilla-extract/css, @pandacss/dev
- **UI Library**: @mui/material, @chakra-ui/react, antd, @radix-ui/themes, @mantine/core, @nextui-org/react, flowbite-react, daisyui
- **CSS Tools**: postcss, autoprefixer, sass, less, stylus

### Tailwind Config
If `tailwindcss` is a dependency, read `tailwind.config.js/ts`:
- `theme.colors` — custom color palette
- `theme.extend.colors` — extended colors
- `theme.borderRadius` — radius tokens
- `theme.boxShadow` — shadow tokens
- `theme.fontFamily` — font definitions
- `theme.spacing` — custom spacing scale
- `plugins` — any plugins that add visual utilities (daisyui, flowbite, etc.)

### Theme Config Files
Look for dedicated theme files:
- `src/theme.js`, `src/theme.ts`, `src/styles/theme.js`
- `src/lib/theme.js`, `src/config/theme.js`
- Any file imported by a `ThemeProvider`, `ConfigProvider`, or similar

---

## Component Semantic Analysis

**This is the critical new layer.** After finding style declarations, you must understand what each styled element *is* and *does*. This prevents mechanical paint from creating visual chaos.

### Step 1 — Identify Component Roles

For every styled component or element, classify it into one of these roles:

| Role | Examples | Visual Weight |
|------|----------|---------------|
| **Navigation** | Navbar, sidebar, breadcrumbs, tabs | High — always visible |
| **Hero / Banner** | Hero sections, splash screens, announcement bars | Highest — first impression |
| **CTA (Call to Action)** | Primary buttons, signup forms, pricing cards | High — conversion critical |
| **Content Display** | Article cards, product cards, list items, tables | Medium — the "body" |
| **Data Visualization** | Charts, graphs, dashboards, stats counters | Medium — content, not chrome |
| **Form / Input** | Text fields, selects, checkboxes, radio buttons | Medium — functional |
| **Feedback** | Toasts, alerts, modals, tooltips, badges | Low-Medium — contextual |
| **Decoration** | Dividers, backgrounds, gradients, patterns | Low — ambiance |
| **Footer / Meta** | Footer, copyright, fine print, breadcrumbs | Low — secondary |

### Step 2 — Group Duplicates

Users often create the same component with different names. You MUST detect and group these:

**Detection signals:**
- Same HTML structure but different class names (`.btn-primary` vs `.main-button` vs `.action-btn`)
- Same visual appearance but different CSS (one uses Tailwind, another uses inline styles)
- Same semantic role in different pages (a "submit" button in checkout vs a "save" button in settings)
- Wrapper components that render the same underlying element with different props

**How to group:**
1. Read the component's rendered output (what HTML does it produce?)
2. Compare visual properties (colors, sizes, spacing)
3. Compare usage context (where is it used? what does it trigger?)
4. If two components serve the same purpose → same group → same paint treatment

**Output format:**
```
Group: Primary Button
  - src/components/Button.tsx (.btn-primary) — used in forms, CTAs
  - src/pages/checkout/Submit.tsx (inline style) — used in checkout
  - src/components/ui/ActionBtn.tsx (.action-btn) — used in dashboard
  Current state: 3 different background colors (#3B82F6, #2563EB, blue-500)
  → Will unify to single primary token
```

### Step 3 — Map Inline Styles to Components

Inline styles are often "quick fixes" that bypass the design system. For each inline style found:
1. Identify which component it belongs to
2. Determine if it's intentional (a one-off override) or accidental (should match the component's class)
3. Link it to the appropriate component group from Step 2

### Step 4 — Flag Inconsistencies

Create a list of all inconsistencies found:

| Type | Example | Impact |
|------|---------|--------|
| **Same role, different colors** | Two primary buttons with different blues | High — confuses users |
| **Same role, different radii** | Cards with mix of 8px and 12px corners | Medium — looks sloppy |
| **Same role, different shadows** | Some cards elevated, same-level cards flat | Medium — breaks hierarchy |
| **Orphan inline styles** | `style={{color: '#666'}}` on a text that should inherit | Low — easy fix |
| **Mixed naming** | `.btn-primary` + `.primary-button` for same thing | Low — code smell |

### Step 5 — Visual Weight Map

Create a hierarchy of visual importance:

```
1. [Highest] Hero sections, primary CTAs
2. [High]    Navigation, key content cards
3. [Medium]  Form elements, secondary buttons, data tables
4. [Low]     Footers, dividers, decorative elements
```

This guides PAINT to prioritize unification — higher-weight components should be treated first, and any inconsistencies in high-weight areas must be resolved before moving to lower-weight items.

---

## CSS & Preprocessor Patterns

### CSS Custom Properties (Variables)
```css
:root {
  --color-primary: #3B82F6;
  --font-body: 'Inter', sans-serif;
  --radius-md: 8px;
  --shadow-sm: 0 1px 2px ...;
}
```
Search pattern: `--` followed by color/font/radius/shadow keywords.

### Hardcoded Color Values
```css
.button { background-color: #3B82F6; }     /* hex */
.card { border: 1px solid rgb(59, 130, 246); } /* rgb */
.text { color: rgba(0, 0, 0, 0.87); }      /* rgba */
.link { color: hsl(217, 91%, 60%); }        /* hsl */
.badge { background: red; }                  /* named color */
```

### Hardcoded Radius Values
```css
.card { border-radius: 8px; }
.button { border-radius: 4px; }
.avatar { border-radius: 50%; }
.pill { border-radius: 9999px; }
```

### Hardcoded Shadow Values
```css
.card { box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1); }
.dropdown { box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1); }
```

### Font Declarations
```css
body { font-family: 'Roboto', sans-serif; }
h1 { font-family: 'Playfair Display', serif; }
```

### Gradient Definitions
```css
.hero { background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); }
.cta { background: radial-gradient(circle, #ff6b6b, #ee5a24); }
```

### SCSS/Less Variables
```scss
$primary-color: #3B82F6;
$border-radius: 8px;
$font-stack: 'Inter', sans-serif;
```
```less
@primary-color: #3B82F6;
@border-radius: 8px;
```

---

## Tailwind Patterns

### Utility Classes in Templates
```jsx
<div className="bg-blue-500 text-white rounded-lg shadow-md border border-gray-200">
<button className="bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-2 px-4 rounded">
<p className="text-gray-600 text-sm font-sans">
```
Look for: `bg-`, `text-`, `border-`, `rounded-`, `shadow-`, `font-`, `ring-` prefixes.

### Tailwind with Arbitrary Values
```jsx
<div className="bg-[#FF2D95] text-[14px] rounded-[8px] shadow-[0_0_10px_rgba(0,0,0,0.1)]">
```
Arbitrary values in square brackets are effectively hardcoded — treat them the same as inline styles.

### Tailwind @apply in CSS
```css
.btn-primary {
  @apply bg-blue-500 text-white rounded-lg shadow-md hover:bg-blue-600;
}
```

### DaisyUI / Plugin Theme Colors
```jsx
<button className="btn btn-primary">
<div className="bg-primary text-primary-content">
```
Check daisyui theme config in `tailwind.config.js` under `daisyui.themes`.

---

## CSS-in-JS Patterns

### styled-components / emotion
```jsx
const Button = styled.button`
  background-color: #3B82F6;
  border-radius: 8px;
  color: white;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
`;
```

### Object-style CSS-in-JS
```jsx
const styles = {
  button: {
    backgroundColor: '#3B82F6',
    borderRadius: '8px',
    color: '#ffffff',
    boxShadow: '0 4px 6px rgba(0, 0, 0, 0.1)',
  }
};
```

### Theme objects (MUI, Chakra, Mantine)
```jsx
// MUI
const theme = createTheme({
  palette: {
    primary: { main: '#3B82F6' },
    secondary: { main: '#10B981' },
  },
  shape: { borderRadius: 8 },
  typography: { fontFamily: 'Inter, sans-serif' },
});

// Chakra
const theme = extendTheme({
  colors: { brand: { 500: '#3B82F6' } },
  radii: { md: '8px' },
  fonts: { body: 'Inter, sans-serif' },
});

// Mantine
const theme = createTheme({
  primaryColor: 'blue',
  colors: { brand: ['#xxx', ...] },
  defaultRadius: 'md',
});
```

---

## Inline Style Patterns

### React JSX
```jsx
<div style={{ color: '#333', backgroundColor: '#f5f5f5', borderRadius: '8px' }}>
<span style={{ fontSize: '14px', fontFamily: 'Inter' }}>
```

### HTML
```html
<div style="color: #333; background-color: #f5f5f5; border-radius: 8px;">
<table bgcolor="#ffffff" cellpadding="10">
```

### Dynamic/Computed Styles
```jsx
<div style={{ backgroundColor: isActive ? '#3B82F6' : '#E5E7EB' }}>
<div style={{ color: theme.colors.primary }}>
```
For dynamic styles, trace the value back to its source (a constant, config, or theme object).

---

## Component Prop Patterns

### UI Library Props
```jsx
// MUI
<Button variant="contained" color="primary">
<TextField variant="outlined" size="small">
<Chip color="success" />

// Chakra
<Button colorScheme="blue" size="md">
<Badge colorScheme="green">
<Input variant="filled">

// Ant Design
<Button type="primary" size="large">
<Tag color="blue">
<Alert type="success">

// shadcn/ui
<Button variant="default" size="default">
<Badge variant="destructive">
```

### Custom Component Props
```jsx
<Card rounded="lg" shadow="md" bg="white">
<Text color="gray.600" fontSize="sm">
<Box bgColor="#f0f0f0" p={4}>
```

---

## SVG & Asset Patterns

### Inline SVG
```jsx
<svg fill="#3B82F6" stroke="#E5E7EB" strokeWidth="2">
  <path fill="#10B981" d="..." />
  <circle fill="none" stroke="#3B82F6" />
</svg>
```

### SVG Files
```xml
<svg xmlns="http://www.w3.org/2000/svg">
  <rect fill="#3B82F6" />
  <text fill="#333333">Label</text>
  <style>
    .cls-1 { fill: #3B82F6; }
  </style>
</svg>
```

### Icon Libraries with Color Props
```jsx
<Icon name="check" color="#10B981" size={24} />
<FaCheck color="green" />
<LuStar fill="#F59E0B" />
```

---

## HTML Patterns

### Meta Theme Color
```html
<meta name="theme-color" content="#3B82F6">
```

### Link/Style Tags
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
```

### Body/HTML Attributes
```html
<body class="bg-white text-gray-900 font-sans">
<html data-theme="light">
```

---

## Regex Reference

```
# Hex colors (3, 4, 6, or 8 digit)
#[0-9a-fA-F]{3,8}\b

# rgb/rgba
rgba?\(\s*\d+

# hsl/hsla
hsla?\(\s*\d+

# Named CSS colors
\b(red|blue|green|white|black|gray|grey|orange|purple|pink|yellow|teal|cyan|indigo|violet)\b

# CSS custom property definitions
--[\w-]+\s*:

# CSS custom property usage
var\(--[\w-]+\)

# font-family declarations
font-family\s*:

# border-radius declarations
border-radius\s*:

# box-shadow declarations
box-shadow\s*:

# Tailwind color classes
(bg|text|border|ring|shadow|outline|fill|stroke|from|via|to|placeholder|divide|accent|caret)-([\w]+-\d+|white|black|transparent|current)

# Tailwind arbitrary values
\[#[0-9a-fA-F]+\]

# SVG fill/stroke
(fill|stroke)=["'][^"']+["']

# Inline style attribute
style\s*=\s*["'\{]

# React style prop
style\s*=\s*\{\{
```

---

## Scan Completion Criteria

Phase 1 is complete when you can answer YES to all of these:

- [ ] Found all CSS/preprocessor files
- [ ] Found all config files (tailwind, theme, postcss)
- [ ] Searched all JS/TS/JSX/TSX files for inline styles
- [ ] Searched all JS/TS/JSX/TSX files for CSS-in-JS
- [ ] Searched all template files for Tailwind classes
- [ ] Searched all template files for component color/style props
- [ ] Searched all SVG files for fill/stroke values
- [ ] Checked HTML files for meta theme-color and font links
- [ ] Identified the project's primary styling approach
- [ ] Listed every unique color value currently in use
- [ ] Listed every font-family currently in use
- [ ] Listed every border-radius value currently in use
- [ ] Listed every box-shadow value currently in use
- [ ] **Classified every styled component by semantic role**
- [ ] **Grouped duplicate/equivalent components**
- [ ] **Flagged all cross-component inconsistencies**
- [ ] **Created visual weight hierarchy map**
