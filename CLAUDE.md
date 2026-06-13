# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the website for **Y Palace**, a 3-star luxury hotel in Ongole, Andhra Pradesh, India, built by Arjun Thotakura. The project is in early development — no framework or build tooling has been set up yet.

Key hotel details:
- Address: Ongole - Kurnool Main Rd, opposite RTC DEPOT, Ongole, AP 523001
- Phone: +91 91543 15190
- Official site: ypalace.in
- 9 room categories (Premium, Elite, Family Suites, Presidential Suites)
- Amenities: Free Wi-Fi, parking, power backup, restaurant, room service, butler service, kids' play area, function hall
- Check-in/out: 12:00 PM

## Assets

Hotel photography lives in [assets/](assets/). There are two tiers:

**Root-level PNGs** (used for hero, about, and main gallery):

| File | Used for |
|---|---|
| `night picture.png` | Hero background, gallery |
| `daytime 1.png` / `daytime 2.png` | Gallery, about section |
| `night.png` / `night 5.png` / `night time 2.png` | Gallery |
| `lunge 1.png` / `lounge 2.png` / `lounge 3.png` | Gallery |
| `room 1.png` / `room 2.png` / `room 3.png` / `room 6.png` / `room 7.png` / `room 8.png` | Gallery |
| `bathroom 1.png` / `bathroom 2.png` | Gallery |
| `funciton hall.png` | Gallery (note the typo in the filename) |
| `entrance.png` | Available, not yet used |

All filenames have spaces — URL-encode as `%20` in `src` attributes.

**Room subdirectories** (used for room cards and gallery modals):

| Subdirectory | Files |
|---|---|
| `assets/premium-rooms-and-washrooms/` | angle1–3.jpeg, pic2–4.jpeg, bathroom–3.jpeg, couch.jpeg, table.jpeg (11 files) |
| `assets/premium-twin-beds/` | angle1–4.jpeg (4 files) |
| `assets/double-king-size-bed-suite-room/` | `Double Kind Size Bed Suite Room.jpeg` × 3 (spaces → `%20`) |
| `assets/suite-room-triple-occupancy/` | angle1–5.jpeg (5 files) |
| `assets/elite-rooms/` | `WhatsApp Image 2026-06-06 at 21.20.36.jpeg` × 3 (spaces → `%20`) |
| `assets/presidential-suite-room/` | `WhatsApp Image 2026-06-06 at 21.20.34.jpeg` (1 file — not yet wired up) |

After any edit that touches `<img src>`, CSS `background-image`, or adds new image references, run a broken-image check before reporting done:

```js
// Quick Playwright check — 0 broken means all naturalWidth > 0
const imgs = await page.locator('img').all();
for (const img of imgs) { const nw = await img.evaluate(el => el.naturalWidth); ... }
```

## Branding

**Always consult [branding-guide.md](branding-guide.md) before creating or editing any webpage.** It defines:
- Color palette (Mocha Brown `#5C3D2E`, Champagne Gold `#C9A84C`, Deep Navy `#1E2640`, Marble Cream `#EDE8DC`, Warm White `#FAFAF7`)
- Typography recommendations (Cormorant Garamond / Playfair Display for headings, Inter/Lato for body)
- Which [assets/](assets/) images to use for each section type (hero, rooms, amenities, etc.)
- Brand voice and copy patterns

## Source Material

[google-review.md](google-review.md) contains aggregated guest review data and hotel information to use as copy for the website.
