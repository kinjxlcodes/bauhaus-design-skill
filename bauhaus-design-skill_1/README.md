# bauhaus-design-skill

> "Form follows function. If an element has no job, it does not exist."

A Claude Code skill encoding 100 years of Bauhaus design thinking as CSS rules,
layout tokens, and component patterns. Makes Claude design like it went to art school.

---

## Install

```bash
npx skills add dotdesxgn/bauhaus-design-skill
```

Install globally across all projects:

```bash
npx skills add dotdesxgn/bauhaus-design-skill -g
```

Install to specific agents:

```bash
npx skills add dotdesxgn/bauhaus-design-skill -a claude-code -a cursor -a windsurf -g
```

Manual install (no npx):

```bash
mkdir -p ~/.claude/skills/bauhaus-design
cp bauhaus-design/SKILL.md ~/.claude/skills/bauhaus-design/
```

---

## Use

Type `/bauhaus` in any Claude Code session.

Auto-triggers when you use words like: `geometric`, `editorial`, `modernist`,
`bauhaus`, `Swiss style`, `form follows function`, `clean UI`, `grid-based`.

---

## What's inside

```
bauhaus-design/
├── SKILL.md        712 lines of Bauhaus design rules for Claude
├── tokens.json     W3C design tokens — import directly into Figma
└── README.md       Skill-level documentation
```

**The skill gives Claude:**
- Full CSS token system — 8 colors, 10 type sizes, 8px grid
- 4 era font pairings — Bauhaus / Industrial / Digital / 2026
- Layout patterns referenced from 4 real design images
- Component library — nav, stamps, pull quotes, tags, status badges
- Animation rules — mechanical precision, zero bounce
- Pre-build checklist — kills AI slop before it happens
- A hard "never do this" list

---

## Works with

Claude Code · Cursor · Windsurf · Gemini CLI · Codex · OpenCode
— any tool that reads `SKILL.md` files.

---

## The four reference aesthetics

| # | Style | Key feature |
|---|-------|-------------|
| 1 | Classic editorial (Fiat 600) | 3-panel grid, vertical date, justified copy |
| 2 | Heavy type grid (IDENTIFONT) | Edge-to-edge display type, 4-col category row |
| 3 | Bauhaus UI components | Primary-color components in circle composition |
| 4 | Geometric architecture | Flat planes, one accent circle, hard shadows |

---

## License

MIT — use, fork, sell. Credit `@dotdesxgn` appreciated.

---

## More from dotdesxgn

Instagram: [@dotdesxgn](https://instagram.com/dotdesxgn) — design + tech + culture
