# WENDZ Website v2

> **Self-contained. No build step. Works by double-clicking.**

---

## Folder Structure

```
wendz-website/
├── index.html              ← Homepage (open this)
├── pages/
│   ├── manifesto.html      ← Brand manifesto
│   └── contact.html        ← Partner application forms
└── README.md
```

All CSS and JS is **inlined inside each HTML file** — no external stylesheet paths, no missing files.

---

## How to Open

**Option A — Just double-click** `index.html` in Finder/Explorer. Works immediately.

**Option B — Local server** (better for development):
```bash
cd wendz-website
python3 -m http.server 3000
# open http://localhost:3000
```

---

## Deploy to GitHub Pages

1. Create a new repository on GitHub
2. Upload (drag-and-drop) the entire `wendz-website/` folder contents
3. Go to **Settings → Pages → Source: Deploy from branch → main → / (root)**
4. Your site is live at `https://yourusername.github.io/wendz-website/`

---

## What's Included

### Animations (all vanilla CSS + JS, zero dependencies)
| Feature | Description |
|---------|-------------|
| Preloader | Full-screen with animated progress bar + letter-by-letter reveal |
| Custom cursor | Dual-ring lerp cursor, changes size on hover |
| Hero text | Staggered line-by-line entrance after preloader |
| Scroll progress | Blue gradient bar at top of viewport |
| Scroll reveals | Fade-up, left, right, scale — IntersectionObserver |
| Counter animation | Eased number counting on scroll |
| Text scramble | Glitch effect on feature headings |
| Marquee | Two infinite scroll banners, pause on hover |
| Hero glow | Mouse-tracked radial background bloom |
| Card tilt | 3D perspective tilt on stat cards |
| Nav behavior | Compact glass nav on scroll |
| Mobile menu | Animated full-screen slide-down |

### Pages
- **Homepage** — Hero, marquee, stats bento, features, journey process, ticker, pull quote, CTA
- **Manifesto** — Brand philosophy, editorial layout, full narrative
- **Contact** — Dual-path partner forms (brands + property owners), HQ section with toast feedback

---

## Customise

### Brand Colours
Inside each `<style>` block at the top of every HTML file:
```css
:root {
  --blue:        #003ec7;
  --blue-bright: #0052ff;
  --ink:         #1a1c1c;
  --paper:       #f9f9f9;
}
```

### Stats Numbers
In `index.html`, find elements with `data-count` and `data-sfx`:
```html
<span class="bc-num" data-count="500000" data-sfx="+">0</span>
```

### Contact Form
Currently shows a toast on submit. To make it live, change the form tag:
```html
<!-- Formspree -->
<form action="https://formspree.io/f/YOUR_ID" method="POST">

<!-- Netlify -->
<form netlify name="brand-application">
```

---

©2025 WENDZ LLP. Stay Quirky.
