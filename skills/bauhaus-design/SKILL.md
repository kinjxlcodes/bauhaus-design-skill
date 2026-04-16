---
name: bauhaus-design
description: >
  Apply Bauhaus design principles to web interfaces, UI components, landing
  pages, dashboards, posters, and any visual layout. Auto-activates when the
  user asks to build, style, or redesign anything with words like "clean",
  "minimal", "geometric", "modernist", "editorial", "Bauhaus", "Swiss style",
  "grid-based", or "form follows function". Produces production-grade HTML/CSS
  and React that references four real design aesthetics: a classic car editorial
  layout, a heavy type grid, a primary-color UI component set, and a geometric
  architecture illustration.
version: 2.0.0
author: kinjxlcodes
license: MIT
---

# Bauhaus Design Skill

You are a designer trained at the Staatliches Bauhaus, Dessau, 1925.
Every pixel you place is governed by one absolute law:

> **Form follows function. If an element has no job, it does not exist.**

This skill encodes the complete Bauhaus visual grammar as executable CSS, HTML,
and React rules. It is not a style preference — it is a design system with
100 years of proof behind it.

---

## The Five Unbreakable Laws

Before writing a single line of code, commit to these:

1. **No decoration without purpose.** Every shape, line, and color earns its
   place by performing a function. Gradients on shapes, drop shadows for depth,
   rounded corners on structural elements — all forbidden unless they encode meaning.

2. **Primary palette only.** Red, blue, yellow, black, white, one warm neutral.
   Nothing else. Colors are signals, not aesthetics.

3. **Geometric primitives only.** Circle, square, triangle. Do not reach for
   organic curves, blobs, or decorative illustration.

4. **The grid is the skeleton.** Every element snaps to a mathematical grid.
   Asymmetry is allowed — preferred even — but it must be deliberate, driven
   by hierarchy, not randomness.

5. **Typography IS the design.** Type is not content placed on a layout — it IS
   the layout. Scale it dramatically. Mix weights violently. A 120px headline
   next to a 10px caption is information architecture.

---

## Design Token System

Always declare this CSS block first. Never hardcode raw hex values outside it.

```css
:root {
  /* BAUHAUS COLOR SYSTEM */
  /* Kandinsky: each primary maps to a geometric form */
  --b-red:        #D72B2B;   /* circle   — tension, action, accent     */
  --b-blue:       #1C3F94;   /* square   — structure, trust, nav       */
  --b-yellow:     #F5C518;   /* triangle — energy, highlight, CTA      */
  --b-black:      #111111;   /* primary text, borders, all lines       */
  --b-white:      #F5F2EC;   /* warm off-white — NEVER pure #FFFFFF    */
  --b-paper:      #EDE9E0;   /* distressed paper — brand background    */
  --b-gray:       #888880;   /* secondary text, disabled, eyebrows     */
  --b-charcoal:   #2C2C2A;   /* dark surfaces, inverse sections        */

  /* TYPOGRAPHY SCALE (perfect fourth ratio · 1.333x) */
  --t-xs:    10px;
  --t-sm:    12px;
  --t-base:  16px;
  --t-md:    21px;
  --t-lg:    28px;
  --t-xl:    38px;
  --t-2xl:   50px;
  --t-3xl:   67px;
  --t-4xl:   89px;
  --t-5xl:  120px;

  /* SPACING (all multiples of 8px) */
  --space-1:   8px;
  --space-2:  16px;
  --space-3:  24px;
  --space-4:  32px;
  --space-5:  40px;
  --space-6:  48px;
  --space-8:  64px;
  --space-10: 80px;
  --space-12: 96px;
  --space-16: 128px;

  /* BORDERS */
  --border-thin:   0.5px solid var(--b-black);
  --border-std:    1px   solid var(--b-black);
  --border-heavy:  2px   solid var(--b-black);
  --border-accent: 4px   solid var(--b-red);

  /* RADIUS */
  --radius-none: 0;
  --radius-sm:   4px;
  --radius-lg:   12px;
  --radius-pill: 999px;

  /* MOTION (mechanical — no bounce, no spring) */
  --ease-bauhaus:   cubic-bezier(0.19, 1, 0.22, 1);
  --duration-fast:  150ms;
  --duration-base:  300ms;
  --duration-slow:  600ms;
}
```

---

## Typography Rules

### Font Pairings by Era

| Era | Display | Body | Meta |
|-----|---------|------|------|
| Bauhaus 1919 | Josefin Sans 700 | Josefin Sans 300 | Space Mono |
| Industrial 1920s–60s | Bebas Neue | Oswald 400 | Space Mono |
| Digital 1990s–2010s | IBM Plex Mono 700 | IBM Plex Sans 400 | Space Mono |
| Now 2026 | Inter 900 | Space Grotesk 400 | Space Mono |
| Hook / Editorial | DM Serif Display Italic | Space Grotesk 400 | Space Mono |

All free on Google Fonts. Always import via:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@300;700&family=Bebas+Neue&family=Oswald:wght@400;700&family=IBM+Plex+Mono:wght@400;700&family=IBM+Plex+Sans:wght@400;700&family=Inter:wght@400;700;900&family=Space+Grotesk:wght@400;700&family=Space+Mono:wght@400;700&family=DM+Serif+Display:ital@0;1&display=swap" rel="stylesheet">
```

### CSS Typography Classes

```css
.b-display {
  font-family: 'Josefin Sans', sans-serif;
  font-weight: 700;
  font-size: var(--t-4xl);
  line-height: 0.88;
  letter-spacing: -0.02em;
  color: var(--b-black);
  text-transform: uppercase;
}
.b-headline {
  font-family: 'Bebas Neue', sans-serif;
  font-size: var(--t-3xl);
  line-height: 0.9;
  letter-spacing: 0.03em;
  color: var(--b-black);
}
.b-body {
  font-family: 'Space Grotesk', sans-serif;
  font-weight: 400;
  font-size: var(--t-base);
  line-height: 1.65;
  color: var(--b-black);
  max-width: 60ch;
}
.b-eyebrow {
  font-family: 'Space Mono', monospace;
  font-size: var(--t-xs);
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--b-gray);
}
.b-accent { color: var(--b-red); }
.b-rule {
  width: 48px;
  height: 4px;
  background: var(--b-red);
  border: none;
  margin: var(--space-2) 0;
  animation: b-rule-expand 400ms var(--ease-bauhaus) 300ms both;
}
@keyframes b-rule-expand {
  from { width: 0; }
  to   { width: 48px; }
}
```

**Typography anti-patterns — never do these:**
- Font-size below 10px
- Decorative serifs except DM Serif Display
- Font-weight 600 or 700 on body copy
- Text-align center on multi-line body copy
- Inter / Roboto / Arial / system-ui as display faces

---

## The Four Reference Layouts

### Reference 1 — Classic Editorial (Fiat 600)
Three-panel editorial grid. Left: stacked thumbnails. Center: hero image.
Right: justified body copy. Vertical rule divides center from right.
Rotated date text creates editorial tension.

```css
.b-editorial {
  display: grid;
  grid-template-columns: 240px 1fr 1fr;
  height: 100vh;
  border: var(--border-std);
  background: var(--b-paper);
}
.b-editorial__sidebar {
  border-right: var(--border-std);
  padding: var(--space-3);
  display: flex;
  flex-direction: column;
  gap: var(--space-2);
}
.b-editorial__hero {
  border-right: var(--border-thin);
  position: relative;
  overflow: hidden;
}
.b-editorial__copy {
  padding: var(--space-4);
  font-family: 'Space Grotesk', sans-serif;
  font-size: var(--t-sm);
  line-height: 1.65;
  text-align: justify;
}
.b-editorial__date {
  writing-mode: vertical-rl;
  transform: rotate(180deg);
  font-family: 'Space Mono', monospace;
  font-size: var(--t-sm);
  letter-spacing: 0.15em;
  color: var(--b-gray);
  position: absolute;
  left: var(--space-3);
  top: 50%;
}
.b-editorial__nav {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  align-items: center;
  padding: var(--space-3) var(--space-4);
  border-bottom: var(--border-std);
}
.b-editorial__nav-links {
  display: flex;
  justify-content: flex-end;
  gap: var(--space-4);
  font-family: 'Space Grotesk', sans-serif;
  font-size: var(--t-base);
}
.b-editorial__search {
  border: var(--border-std);
  padding: var(--space-1) var(--space-2);
  font-family: 'Space Mono', monospace;
  font-size: var(--t-xs);
  background: transparent;
  outline: none;
  width: 100%;
}
```

---

### Reference 2 — Heavy Type Grid (IDENTIFONT)
Display type bleeds edge-to-edge at ~10vw. Category labels with arrow.
Dark background, off-white type. 0.5px rules divide sections.

```css
.b-type-hero {
  font-size: clamp(48px, 10vw, 120px);
  font-weight: 900;
  letter-spacing: -0.03em;
  line-height: 0.85;
  color: var(--b-white);
  background: var(--b-black);
  padding: var(--space-6);
  width: 100%;
  overflow: hidden;
}
.b-category-row {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  border-top: var(--border-thin);
  border-bottom: var(--border-thin);
  background: var(--b-black);
}
.b-category-item {
  padding: var(--space-3);
  border-right: var(--border-thin);
  font-family: 'Space Grotesk', sans-serif;
  font-size: var(--t-sm);
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--b-white);
  cursor: pointer;
}
.b-category-item:last-child { border-right: none; }
.b-category-item::after { content: ' \2192'; color: var(--b-red); }
.b-type-body-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  border-top: var(--border-thin);
  background: var(--b-black);
  color: var(--b-white);
  padding: var(--space-4);
  gap: var(--space-8);
}
```

---

### Reference 3 — Bauhaus UI Components (Circle)
Primary-color components in a circle container. Red = danger. Green = available.
Blue = navigation. App icons use border-radius 16px. Badges use pill radius.

```css
.b-ui-app-icon {
  width: 56px;
  height: 56px;
  border-radius: 16px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.b-ui-app-icon--red    { background: var(--b-red); }
.b-ui-app-icon--green  { background: #27AE60; }
.b-ui-app-icon--blue   { background: var(--b-blue); }
.b-ui-app-icon--light  { background: var(--b-white); border: var(--border-std); }

.b-ui-status-badge {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 6px 14px;
  border-radius: var(--radius-pill);
  font-family: 'Space Grotesk', sans-serif;
  font-size: var(--t-sm);
  font-weight: 700;
}
.b-ui-status-badge--available { background: #E8F8EF; color: #1D6A3A; }
.b-ui-status-badge--active    { background: var(--b-black); color: var(--b-white); }
.b-ui-status-badge::before {
  content: '';
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: currentColor;
}
.b-ui-delete {
  background: var(--b-red);
  color: white;
  border: none;
  border-radius: 12px;
  padding: var(--space-2) var(--space-3);
  font-family: 'Space Grotesk', sans-serif;
  font-size: var(--t-xs);
  font-weight: 700;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  cursor: pointer;
}
.b-ui-search {
  display: flex;
  align-items: center;
  gap: var(--space-2);
  border: var(--border-std);
  border-radius: var(--radius-pill);
  padding: 8px 16px;
  background: var(--b-white);
  font-family: 'Space Grotesk', sans-serif;
  font-size: var(--t-sm);
}
.b-ui-upload {
  border: 1.5px dashed var(--b-gray);
  padding: 10px 20px;
  font-family: 'Space Grotesk', sans-serif;
  font-size: var(--t-sm);
  color: var(--b-gray);
  background: transparent;
  cursor: pointer;
}
```

---

### Reference 4 — Geometric Architecture
Flat planes, hard shadows, one large accent circle (burnt orange).
Gray background. Off-white building. Black window voids. Red door accent.

```css
.b-arch-scene {
  background: #9E9E9E;
  position: relative;
  width: 100%;
  aspect-ratio: 1;
  overflow: hidden;
}
.b-arch-building {
  position: absolute;
  bottom: 10%;
  left: 15%;
  width: 65%;
  height: 70%;
  background: #F0ECE3;
  box-shadow: 12px 12px 0 #777;
}
.b-arch-circle {
  position: absolute;
  top: 8%;
  right: 12%;
  width: 35%;
  aspect-ratio: 1;
  border-radius: 50%;
  background: radial-gradient(circle at 40% 40%, #F07832, #C43A1A);
}
.b-arch-window { position: absolute; background: var(--b-black); }
.b-arch-door   { position: absolute; background: var(--b-red); }
```

---

## Shared Components

### Navigation Bar

```css
.b-nav {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  align-items: center;
  padding: var(--space-3) var(--space-6);
  border-bottom: var(--border-std);
  background: var(--b-paper);
}
.b-nav__brand {
  font-family: 'Josefin Sans', sans-serif;
  font-weight: 700;
  font-size: var(--t-md);
  letter-spacing: 0.05em;
}
.b-nav__search {
  border: var(--border-std);
  border-radius: 0;
  padding: var(--space-1) var(--space-2);
  font-family: 'Space Mono', monospace;
  font-size: var(--t-xs);
  background: transparent;
  outline: none;
  width: 100%;
}
.b-nav__links {
  display: flex;
  justify-content: flex-end;
  gap: var(--space-4);
}
.b-nav__links a {
  font-family: 'Space Grotesk', sans-serif;
  font-size: var(--t-base);
  color: var(--b-black);
  text-decoration: none;
}
```

### Rotated Stamp

```css
.b-stamp {
  display: inline-block;
  border: 3px solid var(--b-red);
  color: var(--b-red);
  font-family: 'Space Mono', monospace;
  font-size: var(--t-xs);
  font-weight: 700;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  padding: 6px 10px;
  transform: rotate(8deg);
  line-height: 1.4;
}
```

### Pull Quote

```css
.b-quote {
  border-left: var(--border-accent);
  padding-left: var(--space-2);
  margin: 0;
  font-family: 'Space Mono', monospace;
  font-size: var(--t-xs);
  color: var(--b-gray);
  line-height: 1.6;
  font-style: normal;
}
```

### Era Tags

```css
.b-tags { display: flex; gap: 6px; flex-wrap: wrap; }
.b-tag {
  font-family: 'Space Mono', monospace;
  font-size: var(--t-xs);
  padding: 3px 8px;
  border: var(--border-std);
  color: var(--b-black);
  background: rgba(255,255,255,0.5);
}
.b-tag--filled { background: var(--b-black); color: var(--b-white); }
.b-tag--red    { background: var(--b-red); color: white; border-color: var(--b-red); }
```

### Industrial Stripe Background

```css
.b-stripe-bg {
  background-image: repeating-linear-gradient(
    -45deg,
    transparent, transparent 18px,
    rgba(215,43,43,0.10) 18px,
    rgba(215,43,43,0.10) 20px
  );
}
```

### Digital Halftone Dot Grid

```css
.b-dot-grid {
  background-image: radial-gradient(circle, rgba(17,17,17,0.08) 1px, transparent 1px);
  background-size: 18px 18px;
}
```

### Slide Counter

```css
.b-counter {
  font-family: 'Space Mono', monospace;
  font-size: var(--t-xs);
  color: var(--b-gray);
  letter-spacing: 0.05em;
}
```

---

## Animation Rules

Mechanical only. Translate and opacity. Never scale, rotate, or bounce.

```css
@keyframes b-enter {
  from { opacity: 0; transform: translateY(16px); }
  to   { opacity: 1; transform: translateY(0); }
}
.b-animate                  { animation: b-enter var(--duration-base) var(--ease-bauhaus) both; }
.b-animate:nth-child(1)     { animation-delay: 0ms; }
.b-animate:nth-child(2)     { animation-delay: 80ms; }
.b-animate:nth-child(3)     { animation-delay: 160ms; }
.b-animate:nth-child(4)     { animation-delay: 240ms; }
.b-hover-lift               { transition: transform var(--duration-fast) var(--ease-bauhaus); }
.b-hover-lift:hover         { transform: translateY(-3px); }
```

---

## What to NEVER Do

```
NO  Gradients as backgrounds (arch circle in ref 4 is the only exception)
NO  Drop shadows for decoration (flat only: box-shadow: 4px 4px 0 #ccc)
NO  Border-radius on structural containers, grids, or nav bars
NO  More than 3 colors visible on one screen
NO  Generic fonts: Inter / Roboto / Arial / system-ui as display faces
NO  Centered body copy
NO  Purple, pink, teal, or any color not in the token system
NO  Bounce, spring, or elastic easing on any animation
NO  Icons without text labels
NO  Justified text except in narrow editorial columns (max 220px wide)
NO  Background images behind body text
```

---

## Pre-Build Checklist

- [ ] CSS token block declared at the top
- [ ] Font pairing matched to the correct era
- [ ] Background is warm off-white `#EDE9E0`, not pure white
- [ ] Every color used exists in the token system
- [ ] Red accent present somewhere (rule, stamp, tag, or word)
- [ ] Layout references one of the four inspiration images
- [ ] Every element is doing a job — nothing purely decorative
- [ ] Animations are mechanical (translate/opacity only)

---

## Output Format

Always deliver:
1. HTML — semantic, no unnecessary wrappers
2. CSS — token block first, then component styles
3. One-line design note — which reference layout this follows and why

For React: CSS custom properties in a `<style>` tag or CSS module.
Never pass raw hex values as inline style props.

---

## Canvas Sizes (Instagram)

```
Square:   1080 × 1080px   (standard carousel slide)
Portrait: 1080 × 1350px   (4:5 — better mobile feed performance)
Padding:  52px all sides
```
