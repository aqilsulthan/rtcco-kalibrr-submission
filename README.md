# Portfolio Website (RTCCO Challenge)

Portfolio website for Cloud Engineer. Built with semantic HTML5 + CSS3, mobile-first, zero JavaScript.

## Tech Stack

- HTML5 (semantic elements only - zero `<div>` layout)
- CSS3 (custom properties, Grid, Flexbox, clamp() fluid typography)
- CSS-only interactions (hamburger menu, project filter, form validation)

## Structure

```
├── index.html              # Portfolio website
├── style.css               # All styles
├── assets/                 # Screenshots + profile images
│   ├── desktop-view.png
│   ├── mobile-view.png
│   ├── ss-web/             # Desktop screenshots (detail)
│   ├── ss-mobile/          # Mobile screenshots (detail)
│   └── foto_aqil.png
└── plan/                   # Process documentation
    ├── 01-brainstorm.md
    ├── 02-details.md
    ├── 03-execution.md
    └── 04-results.md
```

## Key Features

- **Semantic HTML5** - only `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<figure>`, `<blockquote>`, `<footer>`. Zero `<div>` or `<span>` wrappers.
- **Mobile-first** - responsive from 320px to 1440px+, 3 breakpoints (mobile/tablet/desktop).
- **CSS-only interactions** - hamburger menu (checkbox hack), project filter (radio button hack), form validation (`:valid`/`:invalid`).
- **Accessibility** - skip link, aria-label, focus-visible, WCAG contrast >= 4.5:1, prefers-reduced-motion.
- **Design system** - CSS custom properties for colors, typography scale with `clamp()`, spacing, shadows.

## Live Demo

[aqilsulthan.github.io/rtcco-kalibrr-submission](https://aqilsulthan.github.io/rtcco-kalibrr-submission/)
