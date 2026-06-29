# Tech Stack

## Overview

Vanilla static website — no build system, no framework, no dependencies. Everything ships as a single HTML file.

## Stack

- **HTML5** — single `index.html` file contains all markup, styles, and scripts
- **CSS** — embedded in a `<style>` block; uses CSS custom properties (variables) for theming
- **JavaScript** — embedded in a `<script>` block at the bottom of `index.html`; vanilla JS only, no libraries
- **Fonts** — Inter (Google Fonts, loaded via `<link>`)

## No Build Step

There is no package.json, bundler, transpiler, or compilation step. To "build", just edit `index.html` directly.

## Running Locally

Open `index.html` directly in a browser, or serve it with any static file server:

```bash
# Python (recommended)
python3 -m http.server 8080

# Node (if npx is available)
npx serve .
```

## Assets

| Path | Contents |
|------|----------|
| `images/` | Project screenshots (PNG), profile photo (JPEG), and PDF exports |
| `videos/` | MP4 demo recordings for each project |
| `AliMostafa_Ios_CV.docx` | Downloadable resume |

## Browser Support

Targets modern evergreen browsers. Uses:
- CSS `color-mix()`, `clamp()`, `backdrop-filter`, CSS Grid, Flexbox
- `IntersectionObserver` for scroll-reveal animations
- `<video>` with `playsinline` and `preload="none"` for performance
