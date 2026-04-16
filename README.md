# bauhaus-design-skill

> "Form follows function. If an element has no job, it does not exist."

A Claude Code plugin encoding 100 years of Bauhaus design thinking as CSS rules,
layout tokens, and component patterns.

---

## Install via Claude Code (recommended)

Inside any Claude Code session:

```
/plugin marketplace add kinjxlcodes/bauhaus-design-skill
/plugin install bauhaus-design@kinjxlcodes-bauhaus-design-skill
```

## Install via npx

```bash
# Clear credential helper first if on Mac
git config --global credential.helper ""

npx skills add kinjxlcodes/bauhaus-design-skill -a claude-code -g
```

## Manual install

```bash
mkdir -p ~/.claude/skills/bauhaus-design
curl -o ~/.claude/skills/bauhaus-design/SKILL.md \
  https://raw.githubusercontent.com/kinjxlcodes/bauhaus-design-skill/main/skills/bauhaus-design/SKILL.md
```

---

## Use

Type `/bauhaus` in any Claude Code session, or use words like `geometric`,
`editorial`, `modernist`, `form follows function` — it auto-triggers.

---

## Structure

```
bauhaus-design-skill/
├── .claude-plugin/
│   └── plugin.json        Plugin metadata
├── skills/
│   └── bauhaus-design/
│       └── SKILL.md       619 lines of Bauhaus rules
└── README.md
```

## What Claude gets

- CSS token system — 8 colors, 10 type sizes, 8px grid
- 5 era font pairings — Bauhaus / Industrial / Digital / 2026 / Editorial
- 4 reference layout patterns from real design images
- Component library — nav, stamps, pull quotes, tags, status badges
- Animation rules — mechanical precision, zero bounce
- Pre-build checklist + hard never-do list

## License

MIT — use, fork, sell. Credit `@kinjxlcodes` appreciated.
