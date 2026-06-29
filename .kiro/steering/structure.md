# Project Structure

## File Layout

```
portfolio/
├── index.html                  # Entire site — markup, CSS, and JS in one file
├── AliMostafa_Ios_CV.docx      # Downloadable resume (linked from hero section)
├── images/
│   ├── me.jpeg                 # Profile photo (used in header logo + hero avatar)
│   ├── imge8.png               # Al-Fatiha app screenshot (image slider)
│   └── imge1–imge10.pdf        # Legacy PDF screenshots (mostly unused)
└── videos/
    ├── etrip.mp4
    ├── Lavander.mp4
    ├── zoz.mp4
    ├── cab.mp4
    ├── Taflo.mp4
    ├── Delivery.mp4
    ├── Medical.mp4
    ├── Reservations.mp4
    └── zoz.mp4
```

## index.html Structure

The file is organized top-to-bottom with clear section comments:

```
<head>
  CSS variables + reset + component styles (all in one <style> block)
<body>
  <header>       — sticky nav, theme toggle, "Hire Me" CTA
  <main>
    .hero        — name, tagline, action buttons, avatar
    #projects    — grid of <article class="card project"> cards
    #competencies — skills grid
    #experience  — experience list items
    #contact     — contact links + message form
  <footer>
  <script>       — theme toggle, scroll reveal, slider, form handler
```

## Conventions

- **CSS variables** are defined in `:root` (dark mode defaults) and `:root.light` (light mode overrides). Always use var(--token) rather than hardcoded colors.
- **Section IDs** (`#projects`, `#competencies`, `#experience`, `#contact`) are used for nav anchor links — don't rename them.
- **Project cards** follow a consistent pattern: `<article class="card project reveal">` with two children — a content `<div>` (text, tags, links) and a media element (`.phone-frame` video or `.slider-wrapper` images).
- **Scroll reveal** is applied via the `reveal` class; the `IntersectionObserver` in the script block adds `.show` when elements enter the viewport.
- **Theme toggle** adds/removes the `light` class on `<html>` and persists the choice to `localStorage`.
- **Videos** use `preload="none"` for performance — keep this on any new video elements.
- **Tags** use `<span class="tag">` inside `.meta` — keep them short (1–3 words).
