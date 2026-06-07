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

Hotel photography is in [assets/](assets/) organized into four subdirectories — **not** the root `assets/` folder. All image `src` paths must point into these subdirectories:

| Subdirectory | Files |
|---|---|
| `assets/premium-rooms-and-washrooms/` | angle1–3.jpeg, pic2–4.jpeg, bathroom–3.jpeg, couch.jpeg, table.jpeg (11 files) |
| `assets/premium-twin-beds/` | angle1–4.jpeg (4 files) |
| `assets/double-king-size-bed-suite-room/` | `Double Kind Size Bed Suite Room.jpeg` × 3 (filenames have spaces — URL-encode as `%20`) |
| `assets/suite-room-triple-occupancy/` | angle1–5.jpeg (5 files) |

**There are no images at the root `assets/` level.** The old placeholder filenames (`night picture.png`, `room 1.png`, `daytime 2.png`, etc.) **do not exist** and must never be referenced. After any edit that touches `<img src>`, CSS `background-image`, or adds new image references, run a broken-image check before reporting done:

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
