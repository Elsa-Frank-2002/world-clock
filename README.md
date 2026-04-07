# World Clock

A personal world clock built with vanilla HTML, CSS and JavaScript. No frameworks, no dependencies — works entirely in one folder.

**Live demo:** https://elsa-frank-2002.github.io/world-clock

---

## Features

- Live time across up to 5 timezones, updating every second
- Horizontal and vertical layout modes
- Square cards in vertical mode for a clean widget look
- 12hr / 24hr toggle
- Sun and moon icons showing day or night at a glance
- Custom nickname per card (e.g. `sisters_place`, `client-hq`)
- Per-card colour with solid or gradient options
- Global theme colour applied to all cards at once
- Show / hide individual cards (max 5 visible)
- Drag and drop to reorder cards
- Add timezones from 30 cities worldwide
- All settings saved automatically per device/browser
- Dark mode out of the box
- Installable as a PWA on desktop and mobile (works offline)

---

## Installing as an app (PWA)

Once the site is live on GitHub Pages, any visitor can install it as a native-feeling app:

**iPhone / iPad**
1. Open the link in Safari
2. Tap the Share button (box with arrow)
3. Tap "Add to Home Screen"
4. Tap Add — it appears on your home screen like an app

**Android**
1. Open the link in Chrome
2. Tap the 3-dot menu
3. Tap "Add to Home Screen" or "Install App"

**Windows / Mac (Chrome or Edge)**
1. Open the link
2. Click the install icon in the address bar (screen with + symbol)
3. Click Install — it opens in its own window like a desktop app

Each user's settings (layout, colours, nicknames, clock format) are saved privately on their own device.

---

## Uploading to GitHub

Your repo needs these 3 files:

```
world-clock/
├── index.html      ← the app
├── manifest.json   ← makes it installable as a PWA
└── sw.js           ← enables offline use
```

To upload:
1. Go to https://github.com/Elsa-Frank-2002/world-clock
2. Click **Add file → Upload files**
3. Drag all 3 files into the upload box
4. Click **Commit changes**

To enable the live URL:
1. Go to **Settings → Pages**
2. Under Branch, select **main** and click **Save**
3. Wait ~60 seconds — your app is live at https://elsa-frank-2002.github.io/world-clock

---

## Customising default timezones

Open `index.html` and find the `DEFAULT_ZONES` array:

```javascript
const DEFAULT_ZONES = [
  { city: 'Bangalore', tz: 'Asia/Kolkata', label: 'IST', home: true, ... },
  ...
];
```

- Change `city` for the display name
- Change `tz` to any [IANA timezone string](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones)
- Set `home: true` on your home city to highlight it

---

## Built with

Vanilla HTML, CSS and JavaScript — no libraries or frameworks. SVG icons drawn inline.

Built by Elsa Frank as a portfolio project, developed with Claude (Anthropic).
