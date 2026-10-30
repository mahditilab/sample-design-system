---
name: sample-design-system
description: Use when designing or building any page, section or component for this website. Builds only from this design system.
---

# Design system (Orange, built on the starter-paper structure)

The look: friendly, bold and clear. Bright orange accent, Space Grotesk headlines, Inter text, pill buttons, rounded cards with a soft shadow.
Source of truth: `assets/tokens.css` (values) and `assets/components.css` (components). The storybook (`storybook.html`) shows every token and component.

## Hard rules
1. Use tokens only. Never write a colour, font, size, radius, shadow or duration directly in a page. If a value is missing, propose adding a token first.
2. Use existing components before inventing new ones. If a page needs something new, say so, propose it as a component, and add it to `components.css` and the storybook once agreed.
3. One `display` or `h1` per page. Sections use `h2`, items inside sections use `h3`.
4. One primary button per section. The navigation button, the hero button and the closing call to action each count in their own section; a repeated action keeps the same label. Button labels start with a verb.
5. One inverse section per page, used for the closing call to action.
6. Every page works on a phone at 390px wide, with no horizontal scroll and touch targets of at least 44px.
7. Text contrast at least 4.5:1. Errors are shown in words, not colour alone.
8. Motion is subtle: elements rise and fade in once with `data-reveal`. Respect reduced motion.
9. No fake testimonials, reviews or numbers. Placeholders stay visibly marked until replaced with real ones.
10. Images: every image has meaningful `alt` text, uses a ratio token (`--ratio-portrait` 4/5, `--ratio-media` 16/9) and lives in `assets/images/`. Images are shown by the `portrait`, `card__media` and `cover` classes only. The `sample-*.svg` and `portrait-placeholder.svg` files are placeholders to be replaced with real ones.
11. Breakpoints are fixed at 520, 640, 820 and 900px (CSS cannot read tokens in media queries). Do not add new ones without a decision in chat.
12. Link cards (`card--link`) are used where a whole card is one link. Their hover is an accent border and an accent title; nothing else changes.
13. Design decisions are made in Claude chat and recorded in the design system or a prototype. When building (Claude Code), never decide design: if something isn't defined, stop and ask with two or three options.

## Components (class names)
- Layout: `container`, `section`, `section--surface`, `section--inverse`, `section--tight`, `section-head`, `grid grid--2|grid--3`, `split`, `stack`
- Type: `display`, `h1`, `h2`, `h3`, `lead`, `body`, `small`, `eyebrow`, `measure`
- Actions: `btn btn--primary`, `btn btn--secondary`, `btn-row`, `link`
- Blog: `posts` / `post-item` (`post-item__date`, `post-item__body`), `post-meta`, `post-layout`, `prose`, `toc` (`toc__title`)
- Images: `hero__grid` (hero text left, `portrait` right; image stacks below on phones), `card__media` (image at the top of a card, 16:9), `cover` (16:9 image at the top of a post). Files live in `assets/images/`. Every image needs meaningful `alt` text.
- Link card: `card card--feature card--link` (whole card is one link), `section-more` (the "see all" row under a card grid)
- Blocks: `nav`, `hero`, `page-hero`, `card`, `card__icon`, `steps` / `step`, `price` / `price--featured`, `badge`, `list`, `quote`, `faq`, `cta`, `footer`
- Forms: `form`, `form__row`, `field`, `label`, `input`, `field__error`

## Page patterns
- Home: split hero (text left, `portrait` right; two buttons, primary then secondary) · latest posts (`section--surface`, `section-head`, three `card--link` cards with `card__media`, then a `section-more` link to the blog) · about (`split`: eyebrow, `h2` and `lead` left, `list` of traits right) · how I work (`section--surface`, three `steps`) · closing CTA (inverse). Navigation: brand, Home, Blog, Contact and one primary button. About joins the navigation once the page exists.
- Pricing: page hero, plans (3 price cards, one featured), FAQ, closing CTA
- About: page hero, beliefs (split), closing CTA
- Contact: page hero, form + what happens next (split)
- Blog index: page hero, simple list of `post-item` rows inside `posts`, newest first
- Post: page hero with `post-meta`, then `post-layout` with an `article.prose` (max 60 characters wide) and a sticky `toc` on the side; the `toc` moves above the text on phones; closing CTA (inverse)

## Tokens (in `assets/tokens.css`)
Colour, font, weight, tracking, radius, shadow, spacing (`--space-1` to `--space-9`), layout (`--gutter`, `--container`, `--section-pad`, `--hero-pad`, `--hero-width`, `--measure`), type scale (`--text-*`), lines (`--border-width`, `--border-width-strong`), sizes and ratios (`--size-tap`, `--size-tap-min`, `--size-input`, `--size-textarea`, `--size-mark`, `--size-icon`, `--nav-height`, `--toc-width`, `--date-width`, `--portrait-max`, `--ratio-portrait`, `--ratio-media`, `--width-section-head`, `--width-page-hero`, `--width-quote`, `--text-brand`) and motion (`--motion-*`).

## Before you deliver
- [ ] Only tokens and existing components used
- [ ] Phone, tablet and desktop checked; no horizontal scroll
- [ ] One h1, one primary button per section, one inverse section
- [ ] Every image has alt text and a ratio token
- [ ] Contrast and form errors checked
- [ ] Placeholders replaced or clearly marked

## Keeping this skill current
When a decision changes the system (a new token, a new component, a new rule), update this file in the same change. Claude chat should suggest it: "This should go into the design skill."
