# sample-design-system

A design system built on the `starter-paper` structure, in the Orange look: friendly and bold. Space Grotesk for display, Inter for text, warm white background, one orange accent, pill buttons and rounded cards. Rust (the original paper look) and Sage are kept as variants: `storybook-rust.html`, `storybook-sage.html`.

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
