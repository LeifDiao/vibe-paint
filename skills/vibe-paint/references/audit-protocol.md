# Audit Protocol

The AUDIT step runs automatically as the final step of both PAINT and POLISH flows. It is a **mechanical verification** — checking that values are correct, consistent, and accessible. It does not make subjective design decisions (that's POLISH's job).

## Table of Contents
1. [Full Re-scan](#step-1--full-re-scan)
2. [Auto-fix Residuals](#step-2--auto-fix-residuals)
3. [Consistency Check](#step-3--consistency-check)
4. [Accessibility Verification](#step-4--accessibility-verification)
5. [Final Report](#step-5--final-report)

---

## Step 1 — Full Re-scan

Re-run the pattern extraction from the scan checklist. The goal is to find anything that was missed during PAINT or POLISH.

### What to look for

**Leftover hardcoded colors:**
Search for hex, rgb, rgba, hsl values that do NOT match the current style's token values. Common hiding spots:

- Deep-nested component files missed in the first pass
- CSS `@media` blocks with different color values
- CSS `:hover`, `:focus`, `:active`, `::before`, `::after` pseudo-selectors
- Keyframe `@keyframes` animations with color values
- Conditional/ternary expressions in JSX: `isActive ? '#old' : '#old'`
- Default prop values in component definitions: `color = '#old'`
- Test files that render UI (`.test.tsx`, `.spec.tsx`, `.stories.tsx`)
- Storybook files (`*.stories.js`, `*.stories.tsx`)

**Leftover old fonts:**
Search for old `font-family` values anywhere in the project.

**Leftover old radii:**
Check for old pixel values if the project used a different radius scale.

**Leftover old shadows:**
Search for `box-shadow` values that don't match the style's shadow tokens.

### Verification

For each file modified, re-read and confirm:
1. No old color values remain
2. All new values reference tokens (CSS variables, Tailwind config, theme object)
3. The file is syntactically valid (no broken CSS, no mismatched brackets)

---

## Step 2 — Auto-fix Residuals

If the re-scan finds values that should have been replaced:

1. **Fix them immediately** — do not ask the user
2. **Log each fix** — keep a count for the final report
3. **Apply the same token strategy** used in PAINT/POLISH

### Edge case decisions

| Situation | Action |
|-----------|--------|
| Hardcoded color in a test assertion | Skip — test logic, not visual |
| Color in a comment | Skip — doesn't render |
| Color in a console.log | Skip — not visual |
| Color in SVG data URI | Replace — renders visually |
| Color in a disabled/legacy file | Flag in report, don't change |
| Data visualization palette colors | Skip — content, not chrome |

---

## Step 3 — Consistency Check

Verify that the same semantic meaning always maps to the same token value.

### Color consistency
| Semantic Role | Check |
|---------------|-------|
| Primary color | All primary buttons, links, accents use the same value |
| Secondary color | All secondary elements use the same value |
| Success color | All success states, checkmarks, positive indicators |
| Error color | All error states, validation messages, destructive actions |
| Warning color | All warning banners, caution indicators |
| Info color | All info badges, help text highlights |
| Surface color | All card backgrounds, panel backgrounds |
| Border color | All borders use consistent values |
| Text primary | All primary body text |
| Text secondary | All secondary/muted text |

### Typography consistency
- One font family for body text across all components
- One font family for headings (if different from body)
- Consistent font size scale
- Consistent font weight usage (400 body, 600/700 headings)

### Radius consistency
- Same radius for same-level components (all cards same, all buttons same)
- Radius scale: xs < sm < md < lg

### Shadow consistency
- Same shadow for same-level elevation
- Shadow scale progresses: xs (subtle) → xl (dramatic)

---

## Step 4 — Accessibility Verification

### Contrast Ratio Checks

| Combination | Minimum Ratio |
|-------------|---------------|
| Body text on page background | 4.5:1 |
| Body text on card/surface background | 4.5:1 |
| Secondary text on page background | 4.5:1 |
| Secondary text on card background | 4.5:1 |
| Button text on button background (primary) | 4.5:1 |
| Button text on button background (secondary) | 4.5:1 |
| Link text on page background | 4.5:1 |
| Placeholder text on input background | 3:1 |
| Icon on background | 3:1 |
| Border on background | 3:1 |
| Focus indicator on background | 3:1 |

### How to calculate contrast

Use the WCAG relative luminance formula:

```
L = 0.2126 * R + 0.7152 * G + 0.0722 * B
(where R, G, B are linearized sRGB values)

Contrast ratio = (L1 + 0.05) / (L2 + 0.05)
(where L1 is the lighter color's luminance)
```

### Common failures by style category

- **Dark themes** (Synthwave, Cyberpunk, Dark Premium): Secondary text too low contrast on dark backgrounds
- **Pastel themes** (Warm Soft, Candy Pop): Primary colors insufficient contrast against white
- **Glass themes** (Glassmorphism): Text on semi-transparent backgrounds varies
- **Neon themes** (Holographic, Vaporwave): Light-on-light combinations fail

### If Contrast Fails

1. Do NOT skip the style — adjust the specific value
2. Darken light colors or lighten dark colors until ratio is met
3. Prefer adjusting foreground rather than background
4. Note the adjustment in the final report

---

## Step 5 — Final Report

Adapt the report format based on the calling context.

### After PAINT

```markdown
## vibe-paint Complete: [Style Name]

### Summary
- **Files scanned**: X
- **Files modified**: Y
- **Total replacements**: Z
- **Residuals auto-fixed**: N
- **Inconsistencies unified**: M (components grouped in SCAN that were normalized)

### Changes by Category

**Colors**
- Primary: [old] → [new]
- Secondary: [old] → [new]
- Background: [old] → [new]
- Text: [old] → [new]

**Typography**
- Font: [old] → [new]
- Font import: [added/updated]

**Border Radius**
- [summary of changes]

**Shadows**
- [summary of changes]

### Accessibility
- Contrast ratios: ✅ All pass (or ⚠️ list warnings with values)
- Focus indicators: ✅ Preserved (or ⚠️ issues)

### Files Modified
[List grouped by type]

### Notes
- [Edge cases, files skipped and why]
- [Data viz colors intentionally unchanged]
- [Dark/light mode considerations]
```

### After POLISH

```markdown
## vibe-paint Polish Complete: [Style Name or "Custom"]

### Summary
- **Files scanned**: X
- **Files refined**: Y
- **Polish adjustments**: Z (context-aware changes)
- **Audit auto-fixes**: N (mechanical corrections after polish)

### Polish Adjustments (context-aware)
[List each subjective change and why it was made]
- [Component]: [What changed] — [Why it's better for this content]

### Audit Fixes (mechanical)
- Residuals fixed: N
- Consistency corrections: M

### Accessibility
- Contrast ratios: ✅ All pass (or ⚠️ list warnings with values)
- Focus indicators: ✅ Preserved (or ⚠️ issues)

### Files Modified
[List grouped by type]

### Notes
- [Edge cases or components that may benefit from further manual review]
```
