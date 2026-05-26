# Y Palace — Branding Guide

Derived from the hotel's physical signage, interior photography, and exterior shots in [assets/](assets/).

---

## Logo & Wordmark

- **Symbol**: A stylized feather/leaf that forms the letter "Y" — fluid and elegant
- **Wordmark**: "Y Palace" — the Y merges with the feather symbol; "Palace" is set in a refined serif
- **Tagline**: "Luxury Stay" — set in a lighter weight beneath the wordmark
- **Usage on dark backgrounds**: White logo on the brand brown (as seen on the physical signage)
- **Usage on light backgrounds**: Brand brown or deep navy logo

The logo asset does not yet exist as a standalone file — it must be recreated as SVG for web use from the signage photo ([assets/entrance.png](assets/entrance.png)).

---

## Color Palette

| Role | Name | Hex | Source |
|------|------|-----|--------|
| Primary brand | Mocha Brown | `#5C3D2E` | Signage background ([entrance.png](assets/entrance.png)) |
| Accent | Champagne Gold | `#C9A84C` | Room accent lighting & bed runners ([room 1.png](assets/room%201.png)) |
| Warm glow | Amber | `#C97C2A` | Lobby ceiling & lounge lighting ([lunge 1.png](assets/lunge%201.png)) |
| Neutral light | Marble Cream | `#EDE8DC` | Bathroom & floor marble ([bathroom 1.png](assets/bathroom%201.png)) |
| Dark contrast | Deep Navy | `#1E2640` | Night exterior facade ([night picture.png](assets/night%20picture.png)) |
| Surface | Warm White | `#FAFAF7` | Room walls, linens |
| Text default | Charcoal | `#2A2A2A` | Body text |

### Dark Theme Tokens

| CSS Variable | Light Value | Dark Value |
|---|---|---|
| `--bg` | `#FAFAF7` | `#1E2640` |
| `--bg-alt` | `#EDE8DC` | `#16213A` |
| `--text` | `#2A2A2A` | `#EDE8DC` |
| `--text-muted` | `#6B5A50` | `#9A8878` |
| `--heading` | `#5C3D2E` | `#C9A84C` |
| `--accent` | `#C9A84C` | `#C97C2A` |
| `--card-bg` | `#FFFFFF` | `#232E4A` |
| `--footer-bg` | `#3A2418` | `#0E1525` |

### Usage
- **Light backgrounds**: Warm White (`#FAFAF7`), alternating sections in Marble Cream (`#EDE8DC`)
- **Dark backgrounds**: Deep Navy (`#1E2640`), alternating in `#16213A`
- **Headings**: Mocha Brown on light; Champagne Gold on dark
- **CTAs / Buttons**: Champagne Gold background with Charcoal text
- **Accents & dividers**: Amber or Champagne Gold on both themes
- **Hero sections**: Always use the Deep Navy overlay on top of night photography, regardless of theme

---

## Typography

No typeface is locked in the assets, but the logo serif suggests a refined, slightly condensed style. Recommended pairings:

| Role | Suggested Font | Weight |
|------|---------------|--------|
| Display / hero headings | Cormorant Garamond or Playfair Display | 400–600 |
| Section headings | Same as display, or EB Garamond | 500–700 |
| Body copy | Inter or Lato | 400 |
| Taglines / captions | Display font, light weight (300) | 300 |

All of the above are available free on Google Fonts.

---

## Visual Style

### Photography
The [assets/](assets/) folder contains 19 property images:

| Category | Files |
|----------|-------|
| Exterior – night | `night picture.png`, `night time 2.png`, `night.png`, `night 5.png` |
| Exterior – day | `daytime 1.png`, `daytime 2.png` |
| Rooms | `room 1.png`, `room 2.png`, `room 3.png`, `room 6.png`, `room 7.png`, `room 8.png` |
| Bathrooms | `bathroom 1.png`, `bathroom 2.png` |
| Lounge / lobby | `lunge 1.png`, `lounge 2.png`, `lounge 3.png` |
| Function hall | `funciton hall.png` *(note the filename typo)* |
| Signage / entrance | `entrance.png` |

**Art direction notes**:
- Night exterior shots convey grandeur — use these for hero/banner sections
- Room shots have warm gold lighting — crop tightly for card/grid layouts
- Lounge shots show amber-lit luxury — good for "amenities" sections
- Bathroom shots highlight marble finishes — use for premium/suite promotions

### Aesthetic
- Warm luxury, not cold minimalism — lean into golds, ambers, and rich browns
- Classical European-influenced architecture (arched windows, ornate facade) pairs well with serif type
- The lobby features a deity statue (Vishnu) — reflects traditional Indian hospitality values
- Avoid stark white/grey tech aesthetics; prefer warm off-whites and cream

---

## Brand Voice

- **Tone**: Gracious, confident, welcoming — not stuffy or overly formal
- **Positioning**: "Luxury Stay" — accessible luxury for families and business travelers
- **Key messages**: Cleanliness, helpful staff, prime location (opposite RTC Bus Stand), value for money

### Sample copy patterns
- Headlines: "Where Comfort Meets Elegance" / "Ongole's Premier Address"
- CTAs: "Book Your Stay" / "Explore Our Rooms" / "Plan Your Event"
- Avoid: Generic words like "amazing", "best", excessive superlatives without context
