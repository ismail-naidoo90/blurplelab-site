# BlurpleLab Design System

## Brand

- **Name:** BlurpleLab
- **Personality:** Professional, product-driven, curious — dark blurple hero with clean light content sections
- **Location:** Cape Town, South Africa

---

## Colors

| Token | Hex | Usage |
|---|---|---|
| Blurple | `#250b52` | Hero background, section headings, card numbers, row numbers, arrows, hover borders |
| Dark navy | `#0d1b2e` | Nav and footer background, primary body text |
| White | `#ffffff` | Page background, cards, CTA button (on hero) |
| Light background | `#f7f8fc` | Projects section background |
| Card border | `#e2e8f0` | Default card and row borders |
| Card border hover | `#250b52` | Border on card/row hover |
| Primary text | `#0d1b2e` | Body copy, card titles, row names |
| Secondary text | `#64748b` | Descriptions, captions, sublines |
| Light purple accent | `#7c3aed` | Eyebrow labels, category tags |

---

## Typography

- **Font:** Inter (Google Fonts) — used for everything, headings and body
- **No Syne, no condensed or stretched variants, no all-caps headings**
- **Hero heading:** Inter, `font-weight: 800`, `56px`, `letter-spacing: -0.02em`, color `#ffffff`
- **Section headings:** Inter, `font-weight: 700`, `letter-spacing: -0.01em`, color `#250b52`
- **Card headings:** Inter, `font-weight: 600`, color `#0d1b2e`
- **Body:** Inter, `font-weight: 400`, `16px`, color `#64748b`
- **Eyebrow labels:** uppercase, `letter-spacing: 0.08em`, `font-weight: 700`, color `#7c3aed`

---

## Layout

```
┌────────────────────────────────────┐
│ NAV          #0d1b2e               │
├────────────────────────────────────┤
│ HERO         #250b52               │
│   Headline: #ffffff, weight 800    │
│   Subline: rgba(255,255,255,0.75) │
│   CTA: white button, #250b52 text  │
├────────────────────────────────────┤
│ WHAT WE DO   #ffffff               │
│   Heading: #250b52                 │
│   Cards: white, #e2e8f0 border     │
│   Hover: border #250b52            │
├────────────────────────────────────┤
│ PROJECTS     #f7f8fc               │
│   Heading: #250b52                 │
│   Rows: white, #e2e8f0 border      │
│   Hover: left 4px #250b52 border   │
├────────────────────────────────────┤
│ CONTACT      #ffffff               │
├────────────────────────────────────┤
│ FOOTER       #0d1b2e               │
└────────────────────────────────────┘
```

- Max content width: 1100px, centered, padding 28px
- No gradient blobs, no decorative shapes

---

## Components

### Nav
- Fixed, full width, `z-index: 100`
- **On page load / at top:** `background: transparent` — floats over the blurple hero seamlessly
- **On scroll past 60px:** transitions to `background: #0d1b2e` with `box-shadow: 0 1px 12px rgba(0,0,0,0.15)` — `transition: background 0.3s ease`
- Logo: Inter 700, white (visible on both transparent and solid states)
- Links: `rgba(255,255,255,0.65)`, hover `#ffffff`
- CTA "Work with us": `border: 1px solid rgba(255,255,255,0.3)`, white text, hover border brightens
- Mobile menu always uses `#0d1b2e` background

### Hero
- Background `#250b52`, centered, `padding: 152px 28px 100px`
- Eyebrow: `rgba(255,255,255,0.6)`, uppercase
- H1: 56px, weight 800, `#ffffff`, `letter-spacing: -0.02em`
- Subline: `rgba(255,255,255,0.75)`, weight 400
- Primary CTA: `background: #ffffff`, `color: #250b52`, weight 700, `border-radius: 6px`, hover `#f3f4f6`
- Ghost CTA: transparent, white text, `border: 1px solid rgba(255,255,255,0.35)`, hover border brightens

### Focus Cards ("What We Do")
- Section background: `#ffffff`
- Card: white bg, `1px solid #e2e8f0`, `border-radius: 10px`, padding 36px 32px
- Hover: border `#250b52`, shadow `0 4px 20px rgba(37,11,82,0.1)`
- Card number: `#250b52`, weight 700
- Card title: `#0d1b2e`, weight 600
- Card desc: `#64748b`

### Project Rows
- Section background: `#f7f8fc`
- Row: white bg, `1px solid #e2e8f0`, `border-radius: 8px`, shadow `0 1px 3px rgba(0,0,0,0.05)`
- Hover: `translateY(-2px)`, shadow deepens, 4px `#250b52` left border via `::before` pseudo
- Row number: `#250b52`, weight 700
- Row name: `#0d1b2e`, weight 600
- Row tag: `#7c3aed` (light purple accent)
- Row description: `#64748b`
- Arrow link: `#250b52`, hover `#7c3aed`

### Footer
- `#0d1b2e`, `border-top: 1px solid rgba(255,255,255,0.06)`
- "BlurpleLab" left: white, Inter 700
- "Cape Town · 2025" right: `rgba(255,255,255,0.4)`

---

## Pages

| File | Description | Theme |
|---|---|---|
| `index.html` | Homepage | Blurple hero + light content sections |
| `dwelly-prototype.html` | Dwelly property portal prototype | Dwelly brand (untouched) |
| `renovation-calculator.html` | Room renovation cost calculator | Dark BlurpleLab |
| `room-visualiser.html` | AI room visualisation comparison (ChatGPT vs Gemini) | Dark BlurpleLab |
