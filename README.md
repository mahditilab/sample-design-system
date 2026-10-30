# sample-design-system

A design system based on `starter-paper`: editorial, calm, confident. Fraunces for display, Inter for text, warm paper background, one rust accent, square corners.

| File | What it is |
|---|---|
| `assets/tokens.css` | All values: colours, fonts, sizes, radii, motion. Change these to make it yours. |
| `assets/components.css` | All components, built from tokens only |
| `assets/site.js` | Reveal-on-scroll and small behaviours |
| `storybook.html` | Every token and component on one page. Open it first. |
| `SKILL.md` | The design rules, written for Claude |
| `CLAUDE.md` | The context file. Fill in the `[brackets]`, then point every chat or Claude Code session at it. |
| `prototypes/` | Page designs from Claude chat go here |

Rule: build only from tokens and components. A new value goes into `tokens.css` first.
Fonts are self-hosted (SIL Open Font License, licence files in `assets/fonts`).
