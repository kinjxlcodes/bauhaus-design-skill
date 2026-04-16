# bauhaus-design-skill

> "Form follows function. If an element has no job, it does not exist."

A Claude Code skill encoding 100 years of Bauhaus design thinking as CSS rules,
layout tokens, and component patterns. Makes Claude design like it went to art school.

## Install

```bash
npx skills add dotdesxgn/bauhaus-design-skill
```

Global install (works across all projects):

```bash
npx skills add dotdesxgn/bauhaus-design-skill -g
```

Specific agents:

```bash
npx skills add dotdesxgn/bauhaus-design-skill -a claude-code -g
```

## Use

Type `/bauhaus` in any Claude Code session.

Auto-triggers on: `geometric`, `editorial`, `modernist`, `bauhaus`,
`Swiss style`, `form follows function`, `clean UI`, `grid-based`.

## What's inside

```
skills/
└── bauhaus-design/
    ├── SKILL.md        619 lines of Bauhaus design rules for Claude
    └── tokens.json     W3C design tokens — import directly into Figma
```

**The skill gives Claude:**
- Full CSS token system — 8 colors, 10 type sizes, 8px grid
- 5 era font pairings — Bauhaus / Industrial / Digital / 2026 / Editorial
- 4 reference layout patterns from real design images
- Component library — nav, stamps, pull quotes, tags, status badges
- Animation rules — mechanical precision, zero bounce
- Hard "never do this" list — kills AI slop before it happens

## Works with

Claude Code · Cursor · Windsurf · Gemini CLI · Codex · OpenCode
— any tool that reads `SKILL.md` files.

## License

MIT — use, fork, sell. Credit `@dotdesxgn` appreciated.
