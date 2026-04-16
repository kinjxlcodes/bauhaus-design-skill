# bauhaus-design — Claude Skill

> "Form follows function. If an element has no job, it does not exist."

A Claude Code skill that encodes 100 years of Bauhaus design thinking as
executable CSS and layout rules. Drop it into any project and Claude will
produce web interfaces that look like the four reference images:

| Reference | Style |
|-----------|-------|
| Classic Car Editorial | 3-panel grid, vertical date text, justified copy |
| IDENTIFONT Type Grid | Edge-to-edge display type, 4-column category row |
| Bauhaus UI Components | Primary-color components, circle composition |
| Geometric Architecture | Flat planes, one accent circle, hard shadows |

---

## Install — Claude Code

```bash
# Global (works across all projects)
mkdir -p ~/.claude/skills/bauhaus-design
cp SKILL.md ~/.claude/skills/bauhaus-design/

# Project-only
mkdir -p .claude/skills/bauhaus-design
cp SKILL.md .claude/skills/bauhaus-design/
```

## Trigger

Type `/bauhaus` in any Claude Code session, or describe your task with words
like "geometric", "editorial", "Bauhaus", "modernist", "form follows function".

---

## What's included

```
bauhaus-design/
├── SKILL.md          ← Main skill file (drop this into ~/.claude/skills/)
├── tokens.json       ← Design token system in W3C format (Figma-importable)
└── README.md         ← This file
```

## The token system

`tokens.json` follows the W3C Design Token Community Group format and can be
imported directly into Figma via the Tokens Studio plugin. It encodes:

- **8 colors** — Kandinsky primaries + structural neutrals
- **10 type sizes** — perfect fourth ratio scale
- **5 font families** — one per design era
- **8 spacing steps** — all multiples of 8px
- **4 border styles** — from 0.5px editorial rules to 4px red accent bars
- **Motion tokens** — mechanical easing, no bounce

## The design system in one sentence

Red = action. Blue = structure. Yellow = energy.
Black = skeleton. Paper = surface. Grid = law.

---

## Sell this

This skill can be packaged and sold on Gumroad or Lemon Squeezy.
Suggested price: $9–$19 for the skill alone, $29–$49 bundled with
a Figma template using the same token system.

## License

MIT — use, fork, sell, remix. Credit @dotdesxgn appreciated.
