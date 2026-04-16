# bauhaus-design

A Claude skill encoding Bauhaus design principles as executable CSS rules.

## Files

| File | Purpose |
|------|---------|
| `SKILL.md` | Main skill — Claude reads this |
| `tokens.json` | W3C design tokens — import into Figma via Tokens Studio |

## What Claude gets

- CSS token system (8 colors, 10 type sizes, 8px grid)
- 5 era font pairings (Bauhaus / Industrial / Digital / 2026 / Editorial)
- 4 reference layout patterns
- Full component library
- Animation rules (mechanical precision, zero bounce)
- Pre-build checklist + hard "never do" list

## Figma import

Open Tokens Studio plugin → Import → JSON → select `tokens.json`
All colors, sizes, spacing, and motion values load as Figma variables.
