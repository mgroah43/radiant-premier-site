# Handoff: Services Page — Radiant Premier Windows & Doors

## Overview
This is the Services page for **Radiant Premier Windows & Doors**, a premium window and door replacement company serving DFW homeowners. The page showcases their two brand partners (Alside and ProVia), with interactive product explorers, comparison tables, and a final CTA.

## About the Design Files
The `services.html` file in this bundle is a **high-fidelity design reference built in HTML** — a prototype showing the intended look, content, and interactive behavior. The task is to **recreate this design in your existing codebase's framework** (React, Next.js, Vue, etc.) using its established patterns, routing, and component library. Do not ship the HTML file directly.

---

## Fidelity
**High-fidelity.** Pixel-accurate colors, typography, spacing, interactions, and copy are all final. Recreate the UI as close to this reference as possible using your codebase's existing patterns and component system.

---

## Page Sections (in order)

### 1. Sticky Navigation
- Dark navy (`#111E2A`) background, 72px height, sticky top
- Logo: serif "Radiant Premier" + gold uppercase tagline "Windows & Doors"
- Nav links: Home, Our Story, Services (active), + "Get Free Estimate" CTA button (red `#8B1E1E`)
- Right side: gold "Veteran & Minority Owned" badge with star icon + border
- Mobile: hamburger at ≤768px, full-screen overlay menu

### 2. Page Hero
- Background: navy `#1C2A39` with subtle red radial gradient overlay
- Two-column grid (1fr 1fr), 5rem gap, centered, `padding: 7rem 0 6rem`
- Left: gold section label, H1 "Premium Products. Precision Installed.", lead paragraph, two CTA buttons (red filled + white outline)
- Right: image placeholder (360px tall), striped diagonal pattern

### 3. Alside Mezzo® Window Explorer (`#windows`)
White background section. Three sub-sections:

#### 3a. Mezzo Hero
- Two-column grid, H2 + description + 4 stat blocks (U-Factor 0.19, SHGC 0.21, ★ ES, 30%) in a bordered row
- Stats use Playfair Display serif, navy/gold/red colors
- Right: 460px image placeholder
- CTA button below stats

#### 3b. Technology Features (6-up grid)
- 3-column CSS grid (1px gap, neutral background creates divider effect)
- Each cell: `bg: #F7F5F2`, `padding: 2rem 1.8rem`
- Red uppercase label (0.68rem, 0.16em tracking), body text (0.85rem)
- Features: EdgeForce™ Frame, CoreFX™ Composite Reinforcement, Cavity Foam Insulation, Gatekeeper™ Sill Interlock, Defense-Tek™ Locking, HP3™ Sill Dam System

#### 3c. Glass Package Selector (interactive)
- 4-column grid of clickable cards — Tier 1 ClimaTech through Tier 4 ClimaTech PriME
- Default active: Tier 4 (navy bg, gold top-border). Others: bg `#F7F5F2`, neutral top-border
- On click: card highlights with red top-border; detail panel appears below (left-border callout box)
- Detail panel pre-populated with PriME info on load

#### 3d. Window Style Tabs (interactive)
- Tab bar: Double Hung | Sliding | Casement | Awning | Picture & Shapes
- Active tab: red `2px` bottom-border, dark text
- Content panel below: 2-column grid — left: tagline + H3 + description + bullet feature list + CTA button; right: 420px image placeholder
- Default active: Double Hung

### 4. FrameWorks® Color Collection
- bg `#F7F5F2`, `padding: 6rem 0`, `border-top: 1px solid #D6D1C4`
- Section label + H3 + description paragraph
- **Exterior colors** (13 swatches): 44×44px colored squares, 2px radius, hover shows name label, click selects with red outline
- **Interior colors** (9 swatches): same behavior
- Color data (hex values) — see `services.html` `extColorData` and `intColorData` arrays

### 5. ProVia Door Explorer (`#entry-doors`)
bg `#F7F5F2`, `padding: 7rem 0`

#### 5a. Door Hero
- 2-column grid: left has gold "ProVia" tag + H2 + description + 4 badge pills (warranty, energy star, etc.); right 400px placeholder

#### 5b. Door Category Tabs (interactive)
- Tabs: "Entry Doors" | "Patio & Sliding Doors"
- Active: red 3px bottom-border
- Panel below (white, bordered): intro paragraph → 2-column card selector (Legacy™ Steel / Signet® Fiberglass for entry; Endure™ / Aspect™ for patio) → detail section
- Active card: red top-border, white bg. Inactive: neutral top-border, `#F7F5F2` bg
- Detail section: feature bullet list + gold-bordered installation note callout + CTA button + 400px image placeholder
- Default state: Entry Doors tab → Legacy™ card selected

### 6. Brand Partners
- bg `var(--navy)` `#1C2A39`, `padding: 6rem 0`
- Header: gold section label + H2 "Two Brands. Both Chosen on Merit." + gold divider + body text
- 2-column card grid separated by 1.5px gap (bg `rgba(255,255,255,0.06)`)
- Cards: partner name in Playfair Display, gold uppercase sub-label, body copy in `rgba(255,255,255,0.45)`

### 7. Comparison Table
- bg `#F7F5F2`
- `<table>` with 3 columns: "What You Should Expect" | "Typical DFW Contractor" | **Radiant Premier** (highlighted)
- Header row: navy bg for cols 1–2, red bg for col 3
- Highlighted column: `rgba(139,30,30,0.04)` cell bg, bold red "yes" text; "no" column uses `#D6D1C4` color
- 7 data rows (see HTML for content)

### 8. Final CTA
- bg `#111E2A`, centered, `padding: 7rem 0`
- Gold section label, H2, body paragraph, two buttons (red filled + white outline)

### 9. Footer
- bg `#111E2A`, 3-column grid (1.6fr 1fr 1fr): brand block + navigate links + contact info
- Bottom bar: copyright left, tagline right
- Collapses to 1 column on mobile

---

## Design Tokens

```
Colors:
  --bg:           #F7F5F2   (warm off-white, page background)
  --white:        #FFFFFF
  --text:         #181818
  --text-secondary: #5E5E5E
  --red:          #8B1E1E   (primary accent)
  --red-dark:     #6e1818   (hover state)
  --navy:         #1C2A39
  --navy-deep:    #111E2A
  --neutral:      #D6D1C4   (borders, dividers)
  --gold:         #B8903A   (secondary accent)

Typography:
  --font-serif:   'Playfair Display', Georgia, serif  (headings)
  --font-sans:    'Montserrat', Helvetica, sans-serif (body/UI)

  H1: clamp(2.6rem, 5.5vw, 4rem), weight 600
  H2: clamp(2rem, 4vw, 2.8rem), weight 600
  H3: 1.35rem, weight 600
  Body: 16px / 1.7 line-height
  Section label: 0.65rem, weight 700, letter-spacing 0.26em, uppercase, red

Layout:
  --max: 1160px (centered container)
  --radius: 2px (buttons, cards)
  Section padding: 6–7rem 0 desktop, 4rem 0 mobile
  Container padding: 0 2rem

Spacing scale (approximate):
  0.5rem / 0.75rem / 1rem / 1.2rem / 1.5rem / 2rem / 2.5rem / 3rem / 4rem / 5rem / 6rem / 7rem
```

---

## Interactions & Behavior

| Component | Behavior |
|---|---|
| Glass Package cards | Click → highlight card (red top-border on inactive, gold stays on Tier 4) + show detail panel |
| Window Style tabs | Click → switch active tab (red underline) + re-render content panel |
| Door Category tabs | Click → switch active tab + re-render door panel |
| Door Line cards | Click → highlight card + re-render feature detail |
| Color swatches | Hover → show color name; Click → outline with red ring + persist label |
| Nav CTA button | Links to `/#contact` or equivalent contact section |
| Hamburger menu | Toggle full-screen overlay on mobile (≤768px) |
| Buttons hover | `translateY(-1px)` + darken background |
| All transitions | `0.2s ease` unless noted |

---

## State Management

- `activePkg` (0–3): currently selected glass package
- `activeStyle` (0–4): currently selected window style tab
- `activeDoor` (0–1): entry doors vs patio doors tab
- `activeLine` (0–1): selected door product line card
- Active color swatch per group (exterior / interior)
- Mobile menu open/closed

All state is local UI state (no server data fetching required). Initialize with: `activePkg=3`, `activeStyle=0`, `activeDoor=0`, `activeLine=0`.

---

## Data

All product content is embedded in the HTML as JavaScript arrays:

- `styleData[]` — 5 window styles with name, tagline, description, features[], img label
- `pkgDetails[]` — 4 glass package detail strings
- `doorData[]` — 2 door categories, each with `lines[]` containing name, sub, desc, features[], img label
- `extColorData[]` — 13 exterior color swatches (name + hex)
- `intColorData[]` — 9 interior color swatches (name + hex)

These should be moved to a data file (e.g. `services-data.ts`) in the real codebase.

---

## Assets Needed

All imagery is currently **placeholder** (striped SVG pattern with monospace labels). Real photos need to be sourced and dropped in. Placeholder labels describe exactly what each image should show:

| Placeholder | Description |
|---|---|
| Services Hero | Elegant home with large picture windows |
| Mezzo Hero | Alside Mezzo double-hung in bright living room |
| Double Hung / Sliding / Casement / Awning / Picture | Each window style in context |
| ProVia Door Hero | ProVia entry door, dark finish, sidelights, brick exterior |
| Legacy™ / Signet® / Endure™ / Aspect™ | Each door product in context |

Fonts loaded from Google Fonts:
- `Playfair Display` (ital 400/500/600/700)
- `Montserrat` (300/400/500/600/700)

---

## Files in This Bundle

| File | Purpose |
|---|---|
| `services.html` | High-fidelity HTML design reference |
| `README.md` | This document — implementation spec |

---

## Integration Notes for GitHub

1. Move `services.html` into your repo as reference only — do not serve it directly.
2. Recreate each section as a component in your framework of choice.
3. Extract `styleData`, `doorData`, `extColorData`, `intColorData` into a typed data file.
4. Replace image placeholders with real photography as assets become available.
5. The nav and footer are shared with other pages (`index.html`, `story.html`) — reuse existing layout components if available.
6. Contact links point to `index.html#contact` — wire to your actual contact route/anchor.
7. Phone: `(443) 875-7617` | Email: `info@radiantpremierwindows.com`
