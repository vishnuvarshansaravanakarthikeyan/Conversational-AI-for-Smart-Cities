# 🏙️ UrbanMind — Conversational AI for Smart Cities Blog

> A fully self-contained, single-page editorial blog exploring how conversational AI is reshaping urban infrastructure, citizen services, and the future of human-city interaction.

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![No Dependencies](https://img.shields.io/badge/Dependencies-Zero-brightgreen?style=for-the-badge)
![Single File](https://img.shields.io/badge/Build-Single%20File-c8f53b?style=for-the-badge)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Live Demo](#-live-demo)
- [Features](#-features)
- [Page Sections](#-page-sections)
- [Articles Included](#-articles-included)
- [Tech Stack](#-tech-stack)
- [Animations & Interactions](#-animations--interactions)
- [Design System](#-design-system)
- [Typography](#-typography)
- [File Structure](#-file-structure)
- [Getting Started](#-getting-started)
- [Customization Guide](#-customization-guide)
- [Responsive Breakpoints](#-responsive-breakpoints)
- [Browser Support](#-browser-support)
- [Performance Notes](#-performance-notes)
- [License](#-license)

---

## 🌆 Overview

**UrbanMind** is a production-grade, single-file static blog page built with pure HTML, CSS, and vanilla JavaScript — no frameworks, no build tools, no dependencies. Every article, section, and interaction lives on a single page. Nothing redirects. Nothing reloads.

The editorial focus is the emerging intersection of **Conversational AI** and **Smart City infrastructure** — covering civic chatbots, digital twins, emergency dispatch AI, multilingual kiosks, IoT-NLP bridges, and urban energy intelligence.

```
urbanmind-blog.html   ← entire site: ~1 file, ~900 lines
```

---

## 🚀 Live Demo

To run locally, simply open the file in any modern browser:

```bash
# Clone or download the file, then:
open urbanmind-blog.html

# Or serve it locally:
npx serve .
# → http://localhost:3000
```

No build step. No `npm install`. No environment variables. Just open and go.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔄 **Zero Redirects** | Every article, section, and link resolves on the same page |
| 📖 **8 Full Articles** | Complete long-form editorial content, fully readable inline |
| 🎯 **Expandable Articles** | Click any card or list row to expand the full article in place |
| 🤖 **Live Chat Demo** | Animated city AI assistant with cycling conversation loop |
| 🖱️ **Custom Cursor** | Magnetic dual-ring cursor with blend-mode difference effect |
| 🎬 **Page Loader** | Cinematic word-reveal loader with animated progress bar |
| 📊 **Count-Up Stats** | Numbers animate up when scrolled into view |
| 🌊 **Scroll Reveals** | Elements fade and rise into view on scroll |
| 🔤 **Marquee Ticker** | Infinite scrolling topic strip |
| 📱 **Fully Responsive** | Adapts cleanly across mobile, tablet, and desktop |
| 📧 **Newsletter Form** | Functional with inline confirmation feedback |
| 🎨 **SVG Cityscape** | Hand-coded inline SVG skyline illustration |
| 🌐 **Smooth Navigation** | All nav links scroll smoothly to page sections |

---

## 📄 Page Sections

The page is organized into **9 major sections**, all accessible via the fixed navigation bar:

```
┌─────────────────────────────────────────┐
│  NAV        Fixed top bar, always visible│
├─────────────────────────────────────────┤
│  HERO       Title, description, chat demo│
├─────────────────────────────────────────┤
│  MARQUEE    Infinite scrolling ticker    │
├─────────────────────────────────────────┤
│  FEATURED   5-card asymmetric grid       │
├─────────────────────────────────────────┤
│  STATS      4 animated counter metrics  │
├─────────────────────────────────────────┤
│  TOPICS     6 topic cards with glow      │
├─────────────────────────────────────────┤
│  ARTICLES   8 expandable full articles  │
├─────────────────────────────────────────┤
│  ABOUT      Mission + contributor team  │
├─────────────────────────────────────────┤
│  NEWSLETTER Email signup with feedback  │
├─────────────────────────────────────────┤
│  FOOTER     Links scroll to sections    │
└─────────────────────────────────────────┘
```

### Navigation Links

All navigation items use `scrollIntoView` — no `href` page jumps, no new tabs:

| Nav Item | Scrolls To |
|---|---|
| Featured | `#featured` |
| Topics | `#topics` |
| Articles | `#articles` |
| About | `#about` |
| Newsletter | `#newsletter` |
| Subscribe → | `#newsletter` |
| Logo click | Top of page |

---

## 📚 Articles Included

All 8 articles are fully written with subheadings, body paragraphs, pull quotes, and topic tags:

| # | Title | Author | Topic | Read Time |
|---|---|---|---|---|
| 01 | How LLMs Are Becoming the New 311 | Aisha Petrov | Civic AI | 12 min |
| 02 | Digital Twins & Dialogue | Marco Fuentes | Infrastructure | 9 min |
| 03 | Voice-Activated Emergency Response | Dr. Lin Okafor | Health & Safety | 8 min |
| 04 | Ask the Bus: AI Transforms Transit | Yuki Andersen | Mobility | 7 min |
| 05 | Privacy in the Talking City | Ravi Sørensen | Privacy & Ethics | 10 min |
| 06 | The Talking Grid: Urban Energy AI | Dr. Priya Mehta | Climate & Energy | 11 min |
| 07 | Sensor to Sentence: IoT & NLP | Dr. Kenji Walsh | IoT & NLP | 9 min |
| 08 | Multilingual Kiosks | Sofia Nakamura | Inclusion | 8 min |

### Article Expand Behavior

```
User clicks card/row
        ↓
toggleArt() fires
        ↓
All open articles close (CSS max-height: 0)
        ↓
Clicked article opens (CSS max-height: 3000px)
        ↓
Page scrolls to article header (smooth)
```

Only **one article is open at a time**. Clicking an already-open article closes it.

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Markup | Semantic HTML5 |
| Styling | CSS3 (Custom Properties, Grid, Flexbox, Animations) |
| Logic | Vanilla JavaScript (ES6+) |
| Fonts | Google Fonts (Syne, DM Serif Display, Space Mono) |
| Icons | Unicode emoji (no icon library required) |
| Graphics | Inline SVG (hand-coded cityscape) |
| Build | None — open the `.html` file directly |
| Dependencies | **Zero** |

---

## 🎬 Animations & Interactions

### Page Load Sequence

```
0.0s  Loader appears (Urban / Mind word reveal)
0.5s  Progress bar animates across
1.8s  Loader slides up and fades out
      ↓
Hero elements stagger in:
  0.3s  Eyebrow badge fades up
  0.45s Hero title fades up
  0.6s  Description fades up
  0.75s CTA buttons fade up
  0.5s  Chat demo slides in from right
```

### Scroll-Triggered Reveals

Elements with `.reveal` class animate when they enter the viewport:

```css
.reveal {
  opacity: 0;
  transform: translateY(28px);
  transition: opacity .8s cubic-bezier(.16,1,.3,1),
              transform .8s cubic-bezier(.16,1,.3,1);
}
.reveal.vis {
  opacity: 1;
  transform: translateY(0);
}
```

Staggered delays via `.d1`, `.d2`, `.d3`, `.d4` classes (0.1s increments).

### Custom Cursor System

```javascript
// Dot snaps instantly to mouse position
dot.style.left = mx + 'px';

// Ring lags behind with lerp smoothing (15% per frame)
rx += (mx - rx) * .15;
ring.style.left = rx + 'px';
```

Ring expands on hover over interactive elements via `body.hov` class toggle.

### Count-Up Counters

Triggered by `IntersectionObserver` when stats section enters view. Uses cubic ease-out easing:

```javascript
const eased = 1 - Math.pow(1 - progress, 3);
el.textContent = (target * eased).toFixed(decimals);
```

### Live Chat Demo

Cycles through 6 conversation exchanges with:
- 3200ms interval between messages
- Typing indicator (3-dot bounce animation) shown before bot replies
- Messages fade + slide up on insertion
- Oldest messages removed when queue exceeds 4

### Article Expand/Collapse

Pure CSS `max-height` transition (no JavaScript height calculation needed):

```css
.article-body          { max-height: 0;    opacity: 0; transition: max-height .7s, opacity .5s; }
.article-body.open     { max-height: 3000px; opacity: 1; }
```

The `+` toggle rotates `45deg` → becomes `×` when open.

---

## 🎨 Design System

All colors are defined as CSS custom properties on `:root`:

```css
:root {
  --ink:    #0a0d12;   /* Primary text, backgrounds */
  --paper:  #f5f2eb;   /* Page background (warm off-white) */
  --lime:   #c8f53b;   /* Primary accent (electric lime) */
  --cyan:   #3bdfdd;   /* Secondary accent (teal) */
  --muted:  #5a6070;   /* Body text, descriptions */
  --card:   #ffffff;   /* Card backgrounds */
  --border: rgba(10,13,18,.1); /* Subtle borders */
}
```

### Color Usage

| Color | Usage |
|---|---|
| `--ink` | Headings, nav background, dark sections, buttons |
| `--paper` | Page background, section backgrounds |
| `--lime` | Badges, accents, stat numbers, active states, CTA buttons |
| `--cyan` | Secondary gradient accent, window highlights in SVG |
| `--muted` | Body copy, card excerpts, metadata |
| `--border` | Card borders, dividers, subtle separators |

### Easing Curves

```css
--ease-out: cubic-bezier(.16, 1, .3, 1);   /* Snappy deceleration */
--ease-in:  cubic-bezier(.7, 0, .84, 0);   /* Fast exit (loader) */
```

---

## 🔤 Typography

Three typefaces, each with a specific role:

| Font | Weight | Role |
|---|---|---|
| **DM Serif Display** | 400 italic | Body copy, article text, excerpts (editorial warmth) |
| **Syne** | 400–800 | Logo, headings, contributor names (geometric, authoritative) |
| **Space Mono** | 400, 700 | Metadata, tags, nav links, code-adjacent UI (technical, precise) |

### Font Scale

```css
--fs-xl:  clamp(2.6rem, 7vw, 5.5rem);   /* Hero title */
--fs-lg:  clamp(1.6rem, 4vw, 2.8rem);   /* Section titles */
--fs-md:  clamp(1rem,   2vw, 1.25rem);  /* Hero description */
--fs-sm:  0.83rem;                       /* Labels, tags, nav */
```

All headline sizes use fluid `clamp()` scaling — no media query font overrides needed.

---

## 📁 File Structure

```
urbanmind-blog.html
│
├── <head>
│   ├── Google Fonts import (Syne, DM Serif Display, Space Mono)
│   └── <style> (all CSS, ~450 lines)
│       ├── CSS Custom Properties
│       ├── Reset
│       ├── Custom Cursor
│       ├── Noise Overlay
│       ├── Page Loader
│       ├── Navigation
│       ├── Hero Section
│       ├── Marquee
│       ├── Featured Grid
│       ├── Stats Strip
│       ├── Topics Grid
│       ├── Articles (expandable)
│       ├── About Section
│       ├── Newsletter
│       ├── Footer
│       ├── Scroll Reveal utility
│       └── Responsive breakpoints
│
└── <body>
    ├── #loader          Page loader overlay
    ├── #cursor          Custom cursor (dot + ring)
    ├── <nav>            Fixed navigation
    ├── #hero            Hero + chat demo
    ├── .marquee-wrap    Infinite ticker
    ├── #featured        5-card featured grid
    ├── #stats           Animated metric counters
    ├── #topics          6 topic cards
    ├── #articles        8 expandable articles
    │   ├── #art-1  →  LLMs & 311 Services
    │   ├── #art-2  →  Digital Twins
    │   ├── #art-3  →  Emergency Response AI
    │   ├── #art-4  →  Transit AI
    │   ├── #art-5  →  Privacy & Ethics
    │   ├── #art-6  →  Energy Grid AI
    │   ├── #art-7  →  IoT & NLP
    │   └── #art-8  →  Multilingual Kiosks
    ├── #about           Mission + team
    ├── #newsletter      Email signup
    ├── <footer>         Links + copyright
    └── <script>         All JS (~120 lines)
        ├── Loader dismiss
        ├── Custom cursor animation (rAF loop)
        ├── Nav scroll shrink
        ├── IntersectionObserver (reveal)
        ├── IntersectionObserver (count-up)
        ├── toggleArt() — article expand/collapse
        ├── Chat loop (setInterval)
        └── Newsletter submit handler
```

---

## 🚀 Getting Started

### Option 1 — Open Directly

```bash
# Download the file
curl -O https://your-repo-url/urbanmind-blog.html

# Open in browser
open urbanmind-blog.html          # macOS
start urbanmind-blog.html         # Windows
xdg-open urbanmind-blog.html      # Linux
```

### Option 2 — Local Server (recommended for full font loading)

```bash
# Using Python
python3 -m http.server 8080
# → http://localhost:8080/urbanmind-blog.html

# Using Node.js
npx serve .
# → http://localhost:3000

# Using PHP
php -S localhost:8080
# → http://localhost:8080/urbanmind-blog.html
```

### Option 3 — Deploy to GitHub Pages

```bash
# 1. Create a new repository
git init
git add urbanmind-blog.html
git commit -m "Initial commit: UrbanMind blog"

# 2. Push to GitHub
git remote add origin https://github.com/yourusername/urbanmind.git
git push -u origin main

# 3. Enable GitHub Pages
# → Settings → Pages → Source: main branch → /root
# → Rename file to index.html for root URL access
mv urbanmind-blog.html index.html
git add . && git commit -m "Rename to index.html" && git push
```

Your site will be live at `https://yourusername.github.io/urbanmind/`

### Option 4 — Deploy to Netlify (drag & drop)

1. Go to [netlify.com/drop](https://app.netlify.com/drop)
2. Rename `urbanmind-blog.html` → `index.html`
3. Drag the file (or folder) onto the Netlify drop zone
4. Live in under 30 seconds at a `*.netlify.app` URL

---

## 🔧 Customization Guide

### Changing Colors

Edit the CSS variables in `:root` at the top of the `<style>` block:

```css
:root {
  --lime: #c8f53b;   /* Change accent color here */
  --cyan: #3bdfdd;   /* Change secondary accent here */
  --ink:  #0a0d12;   /* Change primary dark color here */
}
```

### Adding a New Article

1. Add a new entry to `#articles` section following this structure:

```html
<div class="article-item" id="art-9">
  <div class="article-header" onclick="toggleArt(this)">
    <div class="art-num">09</div>
    <div>
      <div class="art-title">Your Article Title Here</div>
      <div class="art-meta">Author Name · Date · X min read</div>
    </div>
    <div class="art-right">
      <div class="art-tag">Topic</div>
      <div class="art-toggle">+</div>
    </div>
  </div>
  <div class="article-body">
    <div class="article-inner">
      <p>Your article body content here...</p>
      <h3>Subheading</h3>
      <p>More content...</p>
      <blockquote><p>"Pull quote here." — Attribution</p></blockquote>
      <div class="tag-row">
        <span>Tag1</span><span>Tag2</span>
      </div>
    </div>
  </div>
</div>
```

2. Optionally add a card in `#featured` pointing to it:

```html
<div class="card" onclick="scrollSec('art-9')">
  <div class="card-tag">Category · Month Year</div>
  <h3 class="card-title">Your Article Title</h3>
  <p class="card-excerpt">Short description here.</p>
  <div class="card-meta">
    <span>Author Name</span>
    <div class="card-arrow">↓</div>
  </div>
</div>
```

### Updating Stats

Find the `#stats` section and update `data-t` (target number) and `data-f` (decimal places):

```html
<!-- Integer counter -->
<span class="count" data-t="500">0</span>

<!-- Decimal counter (1 decimal place) -->
<span class="count" data-t="3.7" data-f="1">0</span>
```

### Updating the Chat Demo Messages

Edit the `chatLoop` array in the `<script>` block:

```javascript
const chatLoop = [
  { role: 'bot',  text: 'Your bot message here.' },
  { role: 'user', text: 'Your user message here.' },
  // Add as many as needed — loops infinitely
];
```

### Changing the Marquee Topics

Edit the `<span>` elements inside `.marquee-inner`. The strip is duplicated (items appear twice) to create a seamless loop — update both copies:

```html
<div class="marquee-inner">
  <span>Topic One</span><span>Topic Two</span><!-- ... -->
  <span>Topic One</span><span>Topic Two</span><!-- duplicate for loop -->
</div>
```

### Adjusting Animation Speed

| Effect | CSS Property | Location |
|---|---|---|
| Loader dismiss delay | `setTimeout(..., 1800)` | JS: loader block |
| Scroll reveal | `transition: opacity .8s` | CSS: `.reveal` |
| Article expand | `transition: max-height .7s` | CSS: `.article-body` |
| Chat interval | `setInterval(addMsg, 3200)` | JS: chat loop |
| Marquee speed | `animation: marquee 20s` | CSS: `.marquee-inner` |
| Count-up duration | `const dur = 1600` | JS: count-up block |

---

## 📱 Responsive Breakpoints

| Breakpoint | Layout Changes |
|---|---|
| `> 900px` | Full desktop: 2-col hero, 3-col featured, 4-col stats, 3-col topics |
| `≤ 900px` | Tablet: 1-col hero, 2-col featured (main spans 2), 2-col stats, 2-col topics. Nav links hidden |
| `≤ 600px` | Mobile: 1-col featured, 2-col stats, 1-col topics, simplified article rows, stacked footer |

The nav CTA button remains visible at all breakpoints. The hamburger menu is omitted by design — the Subscribe CTA serves as the primary mobile nav action.

---

## 🌐 Browser Support

| Browser | Support |
|---|---|
| Chrome 90+ | ✅ Full support |
| Firefox 88+ | ✅ Full support |
| Safari 14+ | ✅ Full support |
| Edge 90+ | ✅ Full support |
| Chrome Android | ✅ Full support (cursor hidden on touch) |
| Safari iOS | ✅ Full support (cursor hidden on touch) |
| IE 11 | ❌ Not supported (uses CSS Grid, Custom Properties, `clamp()`) |

> **Note on custom cursor:** On touch devices, the custom cursor elements are present in the DOM but invisible. No layout or functional impact.

---

## ⚡ Performance Notes

- **No external JavaScript** — zero JS payload beyond the file itself
- **Google Fonts** — the only external request (3 font families, ~50KB total). Can be replaced with system fonts or self-hosted for fully offline use
- **No images** — all visuals are inline SVG or CSS gradients; zero image HTTP requests
- **IntersectionObserver** — used for all scroll effects; no scroll event listeners (performant)
- **requestAnimationFrame** — cursor animation runs on rAF loop, not `mousemove` setInterval
- **CSS transitions over JS** — article expand/collapse uses CSS `max-height` transition; no JavaScript layout calculation

### Making It Fully Offline

Replace the Google Fonts `<link>` with locally hosted font files:

```html
<!-- Remove this: -->
<link href="https://fonts.googleapis.com/css2?family=Syne..." rel="stylesheet"/>

<!-- Add this to your <style> block: -->
@font-face {
  font-family: 'Syne';
  src: url('./fonts/Syne-Bold.woff2') format('woff2');
  font-weight: 700;
}
/* Repeat for each weight/family */
```

---

## 📄 License

```
MIT License

Copyright (c) 2025 UrbanMind

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
```

---

<div align="center">

**Built with 🏙️ curiosity and ⚡ vanilla code**

*UrbanMind — Where the city learns to speak*

</div>
