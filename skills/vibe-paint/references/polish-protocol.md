# Polish Protocol

Polish is a **content-aware, context-sensitive** UI refinement process. Unlike PAINT (mechanical token replacement) or AUDIT (mechanical verification), Polish **understands** what the UI is showing and adapts the visual treatment to fit.

PAINT answers: "Are the right colors applied?"
AUDIT answers: "Are the values correct and consistent?"
POLISH answers: "Does the UI *feel* right for this specific content?"

---

## When to Run

- After `/vibe-paint [style]` when the result looks technically correct but visually "off"
- When components are styled correctly in isolation but don't work well together
- When the mechanical token swap produced valid but suboptimal results for the specific content

---

## Step 0 — Detect Current Style

Before anything else, identify which vibe-paint style is currently applied (if any).

**Detection method:**
1. Read CSS variable declarations (`:root`) — match token values against the style-tokens reference
2. Check for vibe-paint comments or markers left by a previous paint (e.g., `/* vibe-paint: synthwave */`)
3. Check Tailwind config or theme file for recognizable token patterns
4. If no vibe-paint style is detected, treat the project as having a custom/unknown style — polish will work with whatever values are present, optimizing for internal consistency rather than conformance to a specific style

**Output:** The detected style slug (e.g., `synthwave`) or `custom` if no match.

---

## Step 1 — Understand the Project

Before touching any code, build a mental model of the project.

### Project Type Identification

| Type | Characteristics | Polish Focus |
|------|----------------|--------------|
| **E-commerce** | Product cards, cart, checkout, pricing | Visual hierarchy of products, CTA prominence, trust signals |
| **Dashboard / Admin** | Data tables, charts, stats, filters | Information density, scanability, data prominence |
| **Blog / Content** | Articles, headings, images, comments | Reading comfort, typography rhythm, content breathing room |
| **SaaS / App** | Forms, workflows, navigation, settings | Clarity of actions, form usability, state communication |
| **Landing Page** | Hero, features, testimonials, CTA | Impact, scroll flow, conversion path |
| **Portfolio** | Gallery, case studies, about | Visual showcase, whitespace, personality |

### Component Purpose Map

For each major component, document:
1. **What it displays** (product info, user data, navigation, etc.)
2. **What action it drives** (buy, navigate, submit, read, etc.)
3. **How important it is** relative to other components on the same page
4. **What emotion it should evoke** (trust, urgency, calm, excitement, etc.)

---

## Step 2 — Evaluate Style Fit

For each component group, assess how well the current style tokens serve the content.

### Questions to Ask

**Color appropriateness:**
- Does the primary color draw attention to the right things?
- Are error/success/warning colors intuitive for this context?
- Are decorative colors enhancing or distracting from content?
- For dark themes: is the contrast comfortable for extended reading?

**Typography fit:**
- Is the font readable at the sizes used in this project?
- Does the heading/body contrast feel right for the content density?
- Are line heights comfortable for the actual text lengths?
- Does the font personality match the content tone? (e.g., a playful font on a financial dashboard feels wrong)

**Spacing and rhythm:**
- Does the radius scale match component sizes? (large radius on small elements looks bloated)
- Do shadows create a sensible depth hierarchy? (is the most elevated thing actually the most important?)
- Is there enough breathing room between content blocks?

**Component-specific:**
- Buttons: Can users instantly tell primary from secondary from ghost?
- Cards: Does the shadow/border treatment reflect content importance?
- Forms: Are inputs clearly distinguishable from static text?
- Navigation: Is the active state obvious? Is hover feedback clear?

### Output

A prioritized list of adjustments needed, grouped by impact:

```
HIGH IMPACT:
- Primary CTA button blends with secondary buttons — increase contrast
- Card shadows too heavy for the content density — reduce to shadow-sm

MEDIUM IMPACT:
- Heading sizes create awkward rhythm with short paragraphs — adjust scale
- Sidebar navigation active state too subtle — strengthen indicator

LOW IMPACT:
- Footer border-top color slightly off from style palette — align to border token
- Badge radius too sharp compared to buttons — unify radius
```

---

## Step 3 — Component-level Refinement

Execute adjustments from the evaluation. Work through each component group.

### Button Hierarchy

Ensure visual clarity of button levels:
```
Primary   → Strongest visual weight (filled, high contrast, prominent shadow)
Secondary → Clearly subordinate (outlined or muted fill, lighter shadow)
Ghost     → Minimal (text only, no fill, subtle hover)
Danger    → Distinct from primary (red family, not confused with CTA)
Disabled  → Obviously inactive (reduced opacity, no hover effect)
```

If the current style's tokens produce ambiguous button levels, adjust:
- Increase fill contrast between primary and secondary
- Add or remove borders to create clearer distinction
- Adjust shadow levels to reinforce hierarchy

### Card & Container Treatment

Match visual weight to content importance:
- **High importance** (featured product, active plan): More elevation (shadow-md/lg), subtle border, possible accent
- **Standard content** (list items, regular cards): Moderate elevation (shadow-sm/md)
- **Background content** (metadata, secondary info): Flat or minimal elevation (shadow-xs or border only)

### Typography Rhythm

Verify the heading → body → caption scale creates comfortable reading:
- H1 should be obviously the page title
- H2 should clearly section the page
- H3 should organize within sections
- Body text should be effortless to read
- Captions/labels should be clearly subordinate without being illegible

If the font from the style doesn't serve the project's content well at certain sizes, adjust:
- Increase body font size if content is text-heavy
- Decrease heading size if headings are very long
- Adjust letter-spacing if the font feels too tight/loose at the used sizes

### Icon & Illustration Harmony

- Do icon stroke weights match the font weight?
- Are icon colors from the token palette or orphaned?
- If the project has illustrations, do their color palettes align with the style?

---

## Step 4 — Layout Integrity

Check that the style changes haven't broken any layouts.

### Overflow Issues
- Elements with `border-radius` changes: rounded corners can clip content on small containers
- Elements with `padding` changes: content may overflow or have too much whitespace
- Elements with `font-size` changes: text may wrap differently, breaking fixed-width layouts

### z-index Conflicts
- Shadow changes can create visual confusion about layer order
- Glassmorphism/blur effects may need z-index adjustments
- Modals, dropdowns, tooltips: verify they still appear above content

### Responsive Behavior
- Check breakpoints: do components stack correctly with new spacing?
- Touch targets: are interactive elements still ≥ 44×44px on mobile?
- Text wrapping: does the new font cause different line breaks at mobile widths?

### Fix Strategy
- If layout is broken → adjust the specific value, don't revert the style
- If overflow occurs → prefer adjusting padding/spacing over changing font/radius
- If z-index is confused → re-establish a clear layer hierarchy

---

## Step 5 — Visual Harmony

The final subjective pass. Look at the UI as a whole.

### Style Fracture Points

Scan for places where the visual style suddenly "breaks":
- A component that looks like it belongs to a different design system
- A color that doesn't appear anywhere else in the palette
- A shadow or radius that doesn't match its siblings
- An animation that feels out of place with the overall style tempo

### Interaction State Consistency

Verify all interactive elements have coherent states:
```
Default  → The resting visual state
Hover    → Clearly different from default (color shift, shadow lift, subtle scale)
Active   → Clearly "pressed" (darker, shadow reduction, scale down)
Focus    → Visible outline/ring (accessibility requirement)
Disabled → Obviously inactive (grayed out, no pointer cursor)
```

All interactive elements should use the same state treatment pattern. If buttons darken on hover, links should also darken (not lighten).

### Animation & Transition Consistency

- All transitions should use the same timing function from the style tokens
- Hover effects should have the same duration across similar components
- If the style has a "fast" personality (cyberpunk, neon), transitions should be quick (150-200ms)
- If the style has a "calm" personality (zen, organic), transitions should be gentle (300-400ms)

---

## Step 6 — AUDIT

After all polish adjustments, run the standard AUDIT protocol.

Read `${CLAUDE_SKILL_DIR}/references/audit-protocol.md` and execute the full audit:
1. Re-scan for residuals
2. Auto-fix any new inconsistencies introduced during polish
3. Consistency check
4. Accessibility verification
5. Final report

The final report should note that this was a POLISH operation and list both:
- Adjustments made during polish (the subjective, context-aware changes)
- Fixes made during audit (the mechanical corrections)
