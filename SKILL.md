---
name: bauhaus-design
description: >
  Apply Bauhaus design principles to web interfaces, UI components, landing
  pages, dashboards, posters, and any visual layout. Auto-activates when the
  user asks to build, style, or redesign anything with words like "clean",
  "minimal", "geometric", "modernist", "editorial", "Bauhaus", "Swiss",
  "grid-based", or "form follows function". Produces production-grade HTML/CSS
  and React that looks like Image 1 (editorial car showcase), Image 2
  (IDENTIFONT heavy type grid), Image 3 (Bauhaus UI components circle), and
  Image 4 (geometric architecture illustration).
version: 2.0.0
author: dotdesxgn
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

Before writing a single line of code, recite these:

1. **No decoration without purpose.** Every shape, line, and color earns its
   place by performing a function. Gradients on shapes, drop shadows for depth,
   rounded corners on structural elements — all forbidden unless they encode
   meaning.

2. **Primary palette only.** Red, blue, yellow, black, white, one warm neutral.
   Nothing else. Colors are not aesthetic choices — they are *signals*.

3. **Geometric primitives only.** Circle, square, triangle. These three shapes
   contain every composition possible. Use them. Do not reach for organic
   curves, blobs, or decorative illustration.

4. **The grid is the skeleton.** Every element snaps to a mathematical grid.
   Asymmetry is *allowed* — in fact it is preferred — but it must be deliberate
   asymmetry driven by hierarchy, not randomness.

5. **Typography IS the design.** Type is not content placed on a layout — it IS
   the layout. Scale it dramatically. Let it break the grid intentionally. Mix
   weights violently. A 120px headline next to a 10px caption is not contrast —
   it is *information architecture*.

---

## Design Token System

Always declare these CSS custom properties first. Never hardcode raw hex values
outside this block. This is your single source of truth — identical to how
Bauhaus masters defined their material palette before touching a canvas.

```css
:root {
  /* ── BAUHAUS COLOR SYSTEM ─────────────────────────────────── */
  /* Kandinsky primaries — each color maps to a geometric form  */
  --b-red:        #D72B2B;   /* circle — tension, action, urgency     */
  --b-blue:       #1C3F94;   /* square — structure, stability, trust  */
  --b-yellow:     #F5C518;   /* triangle — energy, warning, highlight */

  /* Structural neutrals */
  --b-black:      #111111;   /* primary text, borders, rules           */
  --b-white:      #F5F2EC;   /* warm off-white — never pure #FFFFFF    */
  --b-paper:      #EDE9E0;   /* distressed paper — your brand neutral  */
  --b-gray:       #888880;   /* secondary text, disabled states        */
  --b-charcoal:   #2C2C2A;   /* dark surfaces, inverse backgrounds     */

  /* ── TYPOGRAPHY SCALE ────────────────────────────────────── */
  /* Based on a perfect fourth (1.333) ratio — Bauhaus math     */
  --t-xs:    10px;    /* eyebrow, meta, legal                          */
  --t-sm:    12px;    /* captions, tags, pills                         */
  --t-base:  16px;    /* body copy                                     */
  --t-md:    21px;    /* subheadings                                   */
  --t-lg:    28px;    /* section titles                                */
  --t-xl:    38px;    /* card headlines                                */
  --t-2xl:   50px;    /* page sections                                 */
  --t-3xl:   67px;    /* hero subheads                                 */
  --t-4xl:   89px;    /* hero display                                  */
  --t-5xl:  120px;    /* poster/landmark type                          */

  /* ── GRID & SPACING ─────────────────────────────────────── */
  /* Base unit: 8px — all spacing is a multiple of 8            */
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

  /* ── BORDER & STRUCTURE ──────────────────────────────────── */
  --border-thin:   0.5px solid var(--b-black);
  --border-std:    1px   solid var(--b-black);
  --border-heavy:  2px   solid var(--b-black);
  --border-accent: 4px   solid var(--b-red);
  --radius-none:   0;          /* default — Bauhaus hates rounded corners */
  --radius-pill:   999px;      /* only for status badges, never structural */

  /* ── MOTION ─────────────────────────────────────────────── */
  --ease-bauhaus: cubic-bezier(0.19, 1, 0.22, 1);  /* mechanical precision */
  --duration-fast:   150ms;
  --duration-base:   300ms;
  --duration-slow:   600ms;
}
```

---

## Typography Rules

### Font Pairings by Slide/Era

You have four approved pairings. Choose based on the content era:

| Era | Display | Body | Mono/Meta |
|-----|---------|------|-----------|
| **Bauhaus (1919)** | Josefin Sans 700 | Josefin Sans 300 | Space Mono |
| **Industrial (1920s–60s)** | Bebas Neue | Oswald 400 | Space Mono |
| **Digital (1990s–2010s)** | IBM Plex Mono 700 | IBM Plex Sans 400 | Space Mono |
| **Now (2026)** | Inter 900 | Space Grotesk 400 | Space Mono |
| **Hook/Editorial** | DM Serif Display Italic | Space Grotesk 400 | Space Mono |

All fonts are available free on Google Fonts. Always import via:
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@300;700&family=Bebas+Neue&family=Oswald:wght@400;700&family=IBM+Plex+Mono:wght@400;700&family=IBM+Plex+Sans:wght@400;700&family=Inter:wght@400;700;900&family=Space+Grotesk:wght@400;700&family=Space+Mono:wght@400;700&family=DM+Serif+Display:ital@0;1&display=swap" rel="stylesheet">
```

### Typography Application Rules

```css
/* DISPLAY — the structure of the page */
.b-display {
  font-family: 'Josefin Sans', sans-serif;   /* swap per era */
  font-weight: 700;
  font-size: var(--t-4xl);
  line-height: 0.88;
  letter-spacing: -0.02em;
  color: var(--b-black);
  text-transform: uppercase;
}

/* HEADLINE — section anchors */
.b-headline {
  font-family: 'Bebas Neue', sans-serif;
  font-size: var(--t-3xl);
  line-height: 0.9;
  letter-spacing: 0.03em;
  color: var(--b-black);
}

/* BODY — the explanation */
.b-body {
  font-family: 'Space Grotesk', sans-serif;
  font-weight: 400;
  font-size: var(--t-base);
  line-height: 1.65;
  color: var(--b-black);
  max-width: 60ch;  /* never exceed 60 characters per line */
}

/* EYEBROW — the classification */
.b-eyebrow {
  font-family: 'Space Mono', monospace;
  font-weight: 400;
  font-size: var(--t-xs);
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--b-gray);
}

/* ACCENT — the red interrupt */
.b-accent { color: var(--b-red); }

/* RULE — a typographic red bar replaces decorative dividers */
.b-rule {
  width: 48px;
  height: 4px;
  background: var(--b-red);
  border: none;
  margin: var(--space-2) 0;
}
```

**Typography anti-patterns — never do these:**
- No font-size below 10px
- No decorative serifs except DM Serif Display (editorial voice only)
- No italic except DM Serif Display
- No font-weight 600 or 700 on body copy
- No text-align: center on multi-line body copy
- Never use Inter, Roboto, Arial, or system-ui as display fonts

---

## Layout System

### The Bauhaus Grid

Every layout uses a 12-column grid with 8px gutters. Columns are sacred.
Content spans them — never sits between them.

```css
.b-grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: var(--space-3);
  padding: 0 var(--space-6);
  max-width: 1440px;
  margin: 0 auto;
}

/* Common column spans */
.col-4  { grid-column: span 4; }   /* sidebar, card 1/3 */
.col-6  { grid-column: span 6; }   /* 50/50 split */
.col-7  { grid-column: span 7; }   /* editorial main column */
.col-8  { grid-column: span 8; }   /* hero text block */
.col-12 { grid-column: span 12; }  /* full bleed */
```

### Layout Reference: The Four Inspiration Images

**Image 1 — Classic Car Editorial (Fiat 600 layout)**
This is your highest-fidelity reference for web pages. Key rules from this image:
- Left column: stacked thumbnail images with minimal border
- Center column: large hero product image, full height, overlapping grid lines
- Right column: body copy, justified text, small point size
- Vertical rule (`1px solid var(--b-gray)`) divides center from right
- Rotated date text (`writing-mode: vertical-rl`) creates editorial tension
- Navigation: Logo left | Search center | Links right — clean 3-column nav
- No background color — raw paper shows through

```css
/* Editorial 3-panel layout — Image 1 reference */
.b-editorial {
  display: grid;
  grid-template-columns: 240px 1fr 1fr;
  gap: 0;
  height: 100vh;
  border: var(--border-std);
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
}
.b-editorial__date {
  writing-mode: vertical-rl;
  text-orientation: mixed;
  transform: rotate(180deg);
  font-family: 'Space Mono', monospace;
  font-size: var(--t-sm);
  letter-spacing: 0.15em;
  color: var(--b-gray);
  position: absolute;
  left: var(--space-3);
  top: 50%;
}
```

**Image 2 — IDENTIFONT Heavy Type Grid**
Heavy display typography as the entire UI. Rules:
- Display type bleeds edge-to-edge at ~10vw font size
- Category labels use small sans + arrow `→` — never buttons
- Body copy fills left 50% column, recent items fill right 50%
- Thin 0.5px horizontal rules divide sections
- Dark background (#111) with off-white (#F5F2EC) type

```css
/* Heavy type grid — Image 2 reference */
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
}
.b-category-item {
  padding: var(--space-3);
  border-right: var(--border-thin);
  font-family: 'Space Grotesk', sans-serif;
  font-size: var(--t-sm);
  letter-spacing: 0.1em;
  text-transform: uppercase;
  cursor: pointer;
}
.b-category-item:last-child { border-right: none; }
.b-category-item::after { content: ' →'; color: var(--b-red); }
```

**Image 3 — Bauhaus UI Components (Circle Composition)**
UI components arranged inside a large circle. Rules:
- Primary color on interactive elements: red for delete/danger, green for available, blue for navigation
- Rounded rectangles for cards only (radius-lg), never for structural layout
- Typography: **Bauhaus** wordmark in center is the anchor — bold sans, no decoration
- Status indicators: filled circle + label text, never icon-only
- All components float within a `border-radius: 50%` container on light bg

```css
/* Bauhaus UI components — Image 3 reference */
.b-ui-app-icon {
  width: 56px;
  height: 56px;
  border-radius: 16px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
}
.b-ui-app-icon--red    { background: var(--b-red); }
.b-ui-app-icon--green  { background: #27AE60; }
.b-ui-app-icon--blue   { background: var(--b-blue); }

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
.b-ui-status-badge--available {
  background: #E8F8EF;
  color: #1D6A3A;
}
.b-ui-status-badge--active {
  background: var(--b-black);
  color: var(--b-white);
}
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
```

**Image 4 — Geometric Architecture Illustration**
Architectural composition: flat planes, hard shadows, one accent circle.
Rules:
- Background: flat mid-gray (#9E9E9E)
- Building: off-white (#F0ECE3) flat faces, black (#111) window voids
- Accent: single large circle in burnt orange/red — always top-right
- No gradients on architectural elements (circle accent can have subtle gradient)
- Shadow is flat gray, not blur — `box-shadow: 8px 8px 0 #777`
- This pattern is used for: hero sections, loading screens, empty states, poster art

```css
/* Geometric architecture — Image 4 reference */
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
.b-arch-window {
  position: absolute;
  background: var(--b-black);
}
```

---

## Component Library

### Navigation Bar

Always use this pattern. Never a sticky nav with backdrop blur.

```html
<nav class="b-nav">
  <span class="b-nav__brand">Brand</span>
  <div class="b-nav__search">
    <input type="text" placeholder="Search">
  </div>
  <div class="b-nav__links">
    <a href="#">Home</a>
    <a href="#">Gallery</a>
    <a href="#">Contact</a>
  </div>
</nav>
```

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
.b-nav__search input {
  width: 100%;
  border: var(--border-std);
  border-radius: 0;
  padding: var(--space-1) var(--space-2);
  font-family: 'Space Mono', monospace;
  font-size: var(--t-xs);
  background: transparent;
  outline: none;
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

### Slide Counter

Every carousel/section gets a counter: `01 / 05`

```css
.b-counter {
  font-family: 'Space Mono', monospace;
  font-size: var(--t-xs);
  color: var(--b-gray);
  letter-spacing: 0.05em;
}
```

### Stamp / Rotated Tag

For era labels, status indicators, editorial callouts:

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

### Warning Stripe Background

Use behind industrial/factory era content at low opacity:

```css
.b-stripe-bg {
  background-image: repeating-linear-gradient(
    -45deg,
    transparent,
    transparent 18px,
    rgba(215, 43, 43, 0.1) 18px,
    rgba(215, 43, 43, 0.1) 20px
  );
}
```

### Halftone Dot Grid

Use behind digital era content:

```css
.b-dot-grid {
  background-image: radial-gradient(
    circle, rgba(17,17,17,0.08) 1px, transparent 1px
  );
  background-size: 18px 18px;
}
```

### Pull Quote

```html
<blockquote class="b-quote">
  "The ultimate aim of all creative activity is building." — Gropius
</blockquote>
```

```css
.b-quote {
  border-left: 3px solid var(--b-red);
  padding-left: var(--space-2);
  margin: 0;
  font-family: 'Space Mono', monospace;
  font-size: var(--t-xs);
  color: var(--b-gray);
  line-height: 1.6;
  font-style: normal;
}
```

### Era Pill Tags

```html
<div class="b-tags">
  <span class="b-tag">Figma</span>
  <span class="b-tag">CSS grid</span>
  <span class="b-tag">UX/UI</span>
</div>
```

```css
.b-tags { display: flex; gap: 6px; flex-wrap: wrap; }
.b-tag {
  font-family: 'Space Mono', monospace;
  font-size: var(--t-xs);
  padding: 3px 8px;
  border: var(--border-std);
  color: var(--b-black);
  background: rgba(255,255,255,0.5);
  letter-spacing: 0.05em;
}
.b-tag--filled {
  background: var(--b-black);
  color: var(--b-white);
  border-color: var(--b-black);
}
.b-tag--red {
  background: var(--b-red);
  color: white;
  border-color: var(--b-red);
}
```

---

## Animation Rules

Bauhaus movement is **mechanical, not organic**. No bounce, no elastic, no spring.

```css
/* Page load — staggered reveal, left to right */
@keyframes b-enter {
  from { opacity: 0; transform: translateY(16px); }
  to   { opacity: 1; transform: translateY(0); }
}

.b-animate { animation: b-enter var(--duration-base) var(--ease-bauhaus) both; }
.b-animate:nth-child(1) { animation-delay: 0ms; }
.b-animate:nth-child(2) { animation-delay: 80ms; }
.b-animate:nth-child(3) { animation-delay: 160ms; }
.b-animate:nth-child(4) { animation-delay: 240ms; }

/* Red rule expand on load */
@keyframes b-rule-expand {
  from { width: 0; }
  to   { width: 48px; }
}
.b-rule { animation: b-rule-expand 400ms var(--ease-bauhaus) 300ms both; }

/* Hover — translate, not scale */
.b-hover-lift { transition: transform var(--duration-fast) var(--ease-bauhaus); }
.b-hover-lift:hover { transform: translateY(-3px); }

/* Never use: scale(), rotate on hover, bounce easing, blur transitions */
```

---

## What to NEVER Do

These are the Bauhaus violations. Break any of them and restart.

```
❌  Gradients as backgrounds (except the architecture circle in Image 4)
❌  Drop shadows for decoration (flat shadows only: box-shadow: 4px 4px 0 #ccc)
❌  Border-radius on structural elements (cards, grids, containers)
❌  More than 3 colors on one screen (primaries + black/white only)
❌  Generic fonts: Inter, Roboto, Arial, system-ui as display faces
❌  Centered body copy
❌  Background images behind text (use flat color or paper texture)
❌  Animations with bounce, elastic, or spring easing
❌  Purple, pink, teal, or any color not in the token system
❌  Rounded navigation bars or pill-shaped main containers
❌  Icons without labels (text must accompany every action icon)
❌  More than one font per typographic role
❌  Justified text except in narrow editorial columns (max 200px wide)
```

---

## Pre-Build Checklist

Run this before generating any output:

- [ ] Did I declare the CSS token block first?
- [ ] Is the font pairing matched to the correct era?
- [ ] Is the background the warm off-white (#EDE9E0), not pure white?
- [ ] Does every color I used exist in the token system?
- [ ] Is there a red accent somewhere? (Rule, stamp, tag, or word highlight)
- [ ] Does the layout reference one of the four inspiration images?
- [ ] Is every element doing a job, or is any element purely decorative?
- [ ] Are animations mechanical (translate/opacity only, cubic-bezier precision)?

---

## Output Format

When generating code, always deliver:

1. **HTML structure** — semantic, no unnecessary wrappers
2. **CSS** — tokens declared first, then component styles
3. **A short design note** — one sentence explaining which of the four images
   this layout is referencing and why

If generating React, use `style` props for one-off values and CSS modules
or a `<style>` tag for the token block and shared classes.

---

## Installation

### Claude Code (global)
```bash
mkdir -p ~/.claude/skills/bauhaus-design
cp SKILL.md ~/.claude/skills/bauhaus-design/
```

### Claude Code (project-only)
```bash
mkdir -p .claude/skills/bauhaus-design
cp SKILL.md .claude/skills/bauhaus-design/
```

### Trigger manually
Type `/bauhaus` in any Claude Code session.

### Auto-trigger
Claude will auto-load this skill when you use words like:
"Bauhaus", "geometric", "editorial", "modernist", "form follows function",
"grid-based", "minimal web design", "Swiss style", "clean UI".
