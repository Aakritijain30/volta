# Project 2 — Responsive Web Layout
**Volta Electric** | The Art of Fluidity

---

**[→ View Live Here](https://Aakritijain30.github.io/volta)**

## Overview

A fully responsive webpage built **mobile-first** — base CSS targets mobile, then complexity increases progressively for tablet and desktop. No JavaScript. No frameworks. Pure HTML + CSS with the Popover API for navigation.

> *"Build responsive architectures from the content out."*

---

## Implementation Checklist

| Requirement | Implementation |
|---|---|
| `<meta name="viewport">` | ✅ `width=device-width, initial-scale=1` |
| Mobile-first base CSS | ✅ Base styles target mobile, `min-width` queries add complexity |
| Grid (macro layout) | ✅ Hero, models, features, range sections |
| Flexbox (micro components) | ✅ Nav, buttons, stats, footer |
| Fluid units (%, rem, vw) | ✅ Throughout — `clamp()` for spacing & typography |
| Hamburger / Popover nav | ✅ Native Popover API — zero JavaScript |
| Accessible touch targets | ✅ All interactive elements ≥ 44×44px |
| User zoom not restricted | ✅ No `user-scalable=no` — allows up to 500% |
| WCAG compliant | ✅ Focus styles, ARIA labels, semantic landmarks |

---

## Breakpoints

| Name | Min-Width | Purpose |
|---|---|---|
| Mobile | 0px | Base styles — single column |
| Tablet | 600px | 2-column feature grid |
| Tablet L | 768px | Side-by-side hero, 2-col models, footer row |
| Desktop | 1024px | Full multi-column, hero proportions |

> Breakpoints are **bridges, not fences** — designed for content breakage, not device models.

---

## Fluid Typography with `clamp()`

- **Min** — smallest readable size on mobile
- **Fluid** — scales with viewport width (`vw`)
- **Max** — caps at desktop for readability

---

## Popover API Navigation (Zero JS)

- Native browser API — no JavaScript required
- `::backdrop` pseudo-element for overlay
- `@starting-style` for entry animation
- `display: none` on trigger at tablet+ (`min-width: 768px`)

---

## Designing for Thumbs

```
🔴 Orange zone — Hard reach (top corners)
🟢 Green zone  — Easy reach (bottom center)
```

All interactive elements:
- Minimum touch target: **44px × 44px** (WCAG 2.5.5)
- CTA buttons: **56px height**
- Mobile nav links: **56px height**
- No elements placed in hard-reach orange zones on mobile

---

## Accessibility

- `user-scalable=no` **NOT used** — user zoom allowed to 500%
- `:focus-visible` styles for keyboard navigation
- `role="list"` on navigation lists
- `aria-label` on all nav landmarks
- `role="progressbar"` + `aria-valuenow/min/max` on range bars
- `aria-label` + `aria-expanded` + `aria-controls` on hamburger button
- Semantic heading hierarchy: h1 → h2 → h3

---

## CSS Architecture

- **Zero inline styles**
- **BEM methodology** — `.model-card__image`, `.feature-card__title`
- **CSS custom properties** as design tokens
- **No IDs** for styling
- **Print styles** included (`@media print`)

---

## Tools Referenced

- [MDN Web Docs — Popover API](https://developer.mozilla.org/en-US/docs/Web/API/Popover_API)
- [MDN — CSS clamp()](https://developer.mozilla.org/en-US/docs/Web/CSS/clamp)
- [Fluid Type Scale Calculator](https://utopia.fyi)
- [CanIUse — Browser Support](https://caniuse.com)

---
