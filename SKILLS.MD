---
name: frontend-design
description: Create distinctive, production-grade frontend interfaces with high design quality. Use this skill when the user asks to build web components, pages, artifacts, posters, or applications (examples include websites, landing pages, dashboards, React components, HTML/CSS layouts, or when styling/beautifying any web UI). Generates creative, polished code and UI design that avoids generic AI aesthetics.
license: Complete terms in LICENSE.txt
---

This skill guides creation of distinctive, production-grade frontend interfaces that avoid generic "AI slop" aesthetics. Implement real working code with exceptional attention to aesthetic details and creative choices.

The user provides frontend requirements: a component, page, application, or interface to build. They may include context about the purpose, audience, or technical constraints.

## Design Thinking

Before coding, understand the context and commit to a BOLD aesthetic direction:
- **Purpose**: What problem does this interface solve? Who uses it?
- **Tone**: Pick an extreme: brutally minimal, maximalist chaos, retro-futuristic, organic/natural, luxury/refined, playful/toy-like, editorial/magazine, brutalist/raw, art deco/geometric, soft/pastel, industrial/utilitarian, etc. There are so many flavors to choose from. Use these for inspiration but design one that is true to the aesthetic direction.
- **Constraints**: Technical requirements (framework, performance, accessibility).
- **Differentiation**: What makes this UNFORGETTABLE? What's the one thing someone will remember?

**CRITICAL**: Choose a clear conceptual direction and execute it with precision. Bold maximalism and refined minimalism both work - the key is intentionality, not intensity.

Then implement working code (HTML/CSS/JS, React, Vue, etc.) that is:
- Production-grade and functional
- Visually striking and memorable
- Cohesive with a clear aesthetic point-of-view
- Meticulously refined in every detail

## Frontend Aesthetics Guidelines

Focus on:
- **Typography**: Choose fonts that are beautiful, unique, and interesting. Avoid generic fonts like Arial and Inter; opt instead for distinctive choices that elevate the frontend's aesthetics; unexpected, characterful font choices. Pair a distinctive display font with a refined body font.
- **Color & Theme**: Commit to a cohesive aesthetic. Use CSS custom properties (`--color-*`) for consistency across the entire interface. Dominant colors with sharp accents outperform timid, evenly-distributed palettes. Define your palette upfront in `:root` and never hardcode colors inline.
- **Motion**: Use animations for effects and micro-interactions. Prioritize CSS-only solutions for HTML. Use Motion library for React when available. Focus on high-impact moments: one well-orchestrated page load with staggered reveals (`animation-delay`) creates more delight than scattered micro-interactions. Cap `animation-delay` values — with large lists, delays can accumulate to many seconds; clamp to a maximum of ~0.4s. Use scroll-triggering and hover states that surprise.
- **Spatial Composition**: Unexpected layouts. Asymmetry. Overlap. Diagonal flow. Grid-breaking elements. Generous negative space OR controlled density.
- **Backgrounds & Visual Details**: Create atmosphere and depth rather than defaulting to solid colors. Add contextual effects and textures that match the overall aesthetic. Apply creative forms like gradient meshes, noise textures, geometric patterns, layered transparencies, dramatic shadows, decorative borders, custom cursors, and grain overlays.

NEVER use generic AI-generated aesthetics like overused font families (Inter, Roboto, Arial, system fonts), cliched color schemes (particularly purple gradients on white backgrounds), predictable layouts and component patterns, and cookie-cutter design that lacks context-specific character.

Interpret creatively and make unexpected choices that feel genuinely designed for the context. No design should be the same. Vary between light and dark themes, different fonts, different aesthetics. NEVER converge on common choices (Space Grotesk, for example) across generations.

**IMPORTANT**: Match implementation complexity to the aesthetic vision. Maximalist designs need elaborate code with extensive animations and effects. Minimalist or refined designs need restraint, precision, and careful attention to spacing, typography, and subtle details. Elegance comes from executing the vision well.

## React-Specific Best Practices

Apply these when building React interfaces:

- **Memoization**: Wrap expensive computations in `useMemo`. Wrap stable callbacks in `useCallback`. Do NOT memoize trivial values — only memo what genuinely recalculates on every render.
- **Dependency arrays**: Every value used inside a hook must appear in its dependency array. Stale closures are a silent failure mode. If a `setState` function is used inside `useCallback`, it is stable and does not need to be in the dep array, but external variables do.
- **Derived state reset**: If a piece of state (e.g., `expandedId`, `selectedItem`) is tied to a filtered list, use a `useEffect` with the filter/search values as dependencies to reset it when the source changes.
- **Event handler correctness**: All `<button>` elements must have `type="button"` unless they intentionally submit a form. Omitting `type` defaults to `submit`, which reloads the page inside `<form>` wrappers.
- **Keys**: Always use stable, unique `id` fields as React keys — never array indices for lists that can reorder or filter.
- **Animation delay capping**: When rendering large lists with staggered `animation-delay` (e.g., `idx * 50ms`), cap the total with `Math.min(idx * 0.05, 0.4)` to prevent delays of several seconds on large datasets.
- **Clipboard API fallback**: `navigator.clipboard` is undefined in non-HTTPS contexts and some browsers. Always provide a `document.execCommand('copy')` textarea fallback.
- **No `localStorage` in claude.ai artifacts**: `localStorage` and `sessionStorage` are not available in the claude.ai artifact sandbox. Store all state in React state variables.

## Accessibility Checklist

Every production-grade interface must pass these:

- All `<input>` elements have an associated `<label>` (either visible or `.sr-only` visually-hidden)
- All icon-only `<button>` elements have `aria-label` describing their action
- Toggle buttons (`view mode`, `expand/collapse`) use `aria-pressed` or `aria-expanded`
- Toast/notification elements have `role="status"` and `aria-live="polite"`
- Navigation landmark elements (`<nav>`) have `aria-label`
- Filter/toggle button groups have `role="group"` with `aria-label`
- Color contrast meets WCAG AA (4.5:1 for normal text, 3:1 for large text)
- Focus indicators are clearly visible (never `outline: none` without an alternative)
- Semantic HTML is used: `<article>`, `<nav>`, `<header>`, `<main>`, `<footer>`, `<section>`
- Interactive elements are reachable and operable by keyboard alone

## File & Asset Checklist

Before shipping a project:

- All files referenced in HTML (favicon, scripts, stylesheets) actually exist
- Favicon provided in both SVG (scalable) and PNG (fallback) formats — link both in `<head>` with `<link rel="icon" href="favicon.svg" type="image/svg+xml">` and `<link rel="alternate icon" href="favicon.png" type="image/png">`
- Meta description accurately reflects current content (prompt counts, version numbers, etc.)
- README, CHANGELOG, and LICENSE are all present and accurate
- Version numbers are consistent across README badges, HTML meta, and package files

## CSS Architecture Pattern

Use this pattern for maintainable, themeable styles:

```css
:root {
  --color-bg:       #09090E;
  --color-surface:  #111118;
  --color-border:   #1E1E2A;
  --color-accent:   #F59E0B;
  --color-accent-2: #FBBF24;
  --color-text:     #EDEDF5;
  --color-muted:    #7777A0;
  --radius-card:    14px;
  --transition:     all 0.25s cubic-bezier(0.4, 0, 0.2, 1);
}
```

Reference these variables consistently throughout all CSS rules. This makes theming (light/dark toggle, brand overrides) trivial.

Remember: Claude is capable of extraordinary creative work. Don't hold back — show what can truly be created when thinking outside the box and committing fully to a distinctive vision.
