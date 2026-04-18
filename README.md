# 🌐 World Clock

A personal world clock web app — installable as a desktop or mobile widget (PWA).

**Live URL:** https://elsa-frank-2002.github.io/world-clock

---

## Default Timezones

| City | Zone | Badge |
|---|---|---|
| ⭐ Bangalore (Home) | Asia/Kolkata | IST |
| Dubai | Asia/Dubai | GST |
| UTC | UTC | UTC |
| São Paulo | America/Sao_Paulo | BRT |
| Chicago | America/Chicago | CDT |

---

## Features

### Display
- Live time updating every second
- ☀️ / 🌙 sun/moon icons for day vs night per city
- Date display per card (weekday, day, month)
- UTC offset shown on every card
- Bangalore marked as home with a ★ star and blue border

### Theme & Appearance
- **Dark mode** — deep navy palette (default)
- **Light mode** — clean white/grey palette
- **Custom background** — choose any colour for the entire app
  - 12 curated preset swatches (Midnight, Abyss, Forest, Plum, Ocean, etc.)
  - Free-pick colour wheel for any hex colour
  - Cards and panels adapt automatically to match
  - Live preview before applying
- Theme selection saved per-device

### Layout / View
Five grid options toggled from the toolbar:

| Button | Mode | Description |
|---|---|---|
| ⊞ | Auto-fit | Cards fill the row responsively (default) |
| ☰ | Single column | Stacked vertical cards |
| ⊞ | 2-column grid | Fixed two columns |
| ⊞ | 3-column grid | Fixed three columns |
| ⊞ | 4-column grid | Fixed four columns |

On mobile, 3-col and 4-col automatically collapse to 2 columns.

### Clock Format
- **24h** (default) and **12h** toggle in the toolbar
- AM/PM shown small beside the time in 12h mode

### Cards
- City name + timezone badge on the same row
- Custom nickname field below the city name
  - Click ✏️ to open an inline editor
  - Stays open until Save, Enter, or Cancel
  - Max 20 characters — letters, numbers, `-` and `_` only
  - Live character counter while typing
- 🎨 Palette icon — set a solid colour or gradient per card
- 👁 Eye icon — show/hide the card (hidden cards stay faded in the list)
- ✕ Remove icon (non-home cards only)
- Drag and drop to reorder cards

### Card Colours
- Per-card colour picker (solid or gradient)
- **Gradient:** pick two colours, choose direction (→ ↓ ↘ ↙), live preview
- **"Theme colour for all cards"** option in the ⋯ Menu applies a colour to every card at once

### Timezone Management
- Up to 10 timezones (5 visible by default, hidden ones stay faded)
- Add from a list of 30 cities worldwide
- Optional custom display name when adding
- **Reset all to default** option in ⋯ Menu

### Save / Restore
- All settings auto-saved to `localStorage` on every change
- Saves: layout, clock format, theme, custom background, card order, visibility, colours, nicknames
- Per-device / per-browser — each user keeps their own settings independently
- ✓ Saved toast confirmation on every change

### PWA — Installable as an App
- Works offline via service worker (`sw.js`)
- Installable on:
  - **iPhone / iPad** — Safari → Share → Add to Home Screen
  - **Android** — Chrome → ⋮ → Install app
  - **Windows / Mac** — Chrome or Edge → install icon in address bar

---

## Files

| File | Purpose |
|---|---|
| `index.html` | Entire app — HTML, CSS, JavaScript (single file) |
| `manifest.json` | PWA metadata for install prompt |
| `sw.js` | Service worker for offline support |
| `README.md` | This file |

---

## Setup / Deployment

No build step required — it's a single HTML file.

```bash
# Clone the repo
git clone https://github.com/Elsa-Frank-2002/world-clock.git
cd world-clock

# Open locally
open index.html          # macOS
start index.html         # Windows
```

For the PWA features (offline, install prompt) to work you need to serve over HTTPS — GitHub Pages does this automatically.

```bash
# Deploy: just push to main, GitHub Pages serves it
git add .
git commit -m "Update"
git push
```

---

## Repo Structure

```
world-clock/
├── index.html       ← entire app
├── manifest.json    ← PWA install metadata
├── sw.js            ← service worker (offline cache)
└── README.md
```

---

## Tech Stack

Vanilla HTML · CSS custom properties · JavaScript (no frameworks, no build tools)

---

*Made with ☕ — deploy it, install it, make it yours.*
