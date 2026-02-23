# Bento Grid

## Project

Static single-page bento grid layout. No frameworks, no build tools, no JavaScript.

## Files

```
  index.html          # Single page, 8 grid cards inside <main class="bento">
  style.css           # All styles, mobile-first with one breakpoint at 768px
  assets/fonts/       # DM Sans variable font (.ttf), regular + italic
  assets/images/      # 8 webp illustrations + favicon
  design/             # Reference screenshots (mobile + desktop)
```

## Grid Layout

Container: `.bento` uses CSS Grid with `grid-template-areas`.

**Area names:** hero, accounts, schedule, timing, followers, growth, create, ai

**Mobile (default):** Single column, areas stacked in this order:
hero, accounts, schedule, timing, followers, growth, create, ai

**Desktop (min-width: 768px):** 4 columns × 3 rows:
```
create   hero      hero      timing
create   accounts  schedule  timing
ai       growth    followers followers
```
Each card class maps directly: `.card-hero` → `grid-area: hero`, etc.

## Color Palette (CSS custom properties in :root)

| Variable         | Value                |
|------------------|----------------------|
| `--purple-100`   | hsl(254, 88%, 90%)   |
| `--purple-500`   | hsl(256, 67%, 59%)   |
| `--yellow-100`   | hsl(31, 66%, 93%)    |
| `--yellow-500`   | hsl(39, 100%, 71%)   |
| `--white`        | hsl(0, 0%, 100%)     |
| `--black`        | hsl(0, 0%, 7%)       |

Body background: `#f5f3f0`

## Typography

- Font: DM Sans (variable, loaded locally via @font-face)
- Weights used: 400 (regular), 500 (medium)
- Base font size: 18px

## Conventions

- Mobile-first: base styles are mobile, desktop overrides via `@media (min-width: 768px)`
- Images set to `max-width: 100%; display: block` globally
- Standard CSS reset (margin/padding/box-sizing) at top of stylesheet
- Max container width: 1200px (centered with `margin: 0 auto`)

## Design Targets

- Mobile: 375px
- Desktop: 1440px
