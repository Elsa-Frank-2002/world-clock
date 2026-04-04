# World Clock

A lightweight, customisable world clock built with HTML, CSS, and JavaScript. No frameworks, no dependencies — just one file that works anywhere.

Live demo: [https://elsa-frank-2002.github.io/world-clock](https://elsa-frank-2002.github.io/world-clock)

---

## Features

- Live time display across up to 5 timezones simultaneously
- Horizontal and vertical layout modes
- Square cards in vertical mode for a clean widget-style look
- 12hr / 24hr clock toggle
- Sun and moon icons showing daytime or nighttime at a glance
- Per-card colour customisation with solid or gradient options
- Global theme colour applied to all cards at once
- Show / hide individual timezone cards
- Drag and drop to reorder cards
- Add timezones from a list of 30 cities worldwide
- Dark mode support out of the box
- Mobile friendly — works as a saved web app on your phone

---

## How to use

### View it live
Visit the live demo link above — no installation needed.

### Run it locally
1. Download or clone this repository
2. Open `index.html` in any browser
3. That's it!

```bash
git clone https://github.com/Elsa-Frank-2002/world-clock.git
cd world-clock
open index.html
```

---

## Project structure

```
world-clock/
└── index.html    # Everything lives here — HTML, CSS, and JavaScript
```

---

## Customisation

To change the default timezones, open `index.html` and find the `zones` array near the top of the script section:

```javascript
let zones = [
  { city: 'Bangalore', tz: 'Asia/Kolkata', label: 'IST', home: true, visible: true, bg: null },
  { city: 'Dubai',     tz: 'Asia/Dubai',   label: 'GST', home: false, visible: true, bg: null },
  ...
];
```

- Change `city` to update the display name
- Change `tz` to any valid [IANA timezone string](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones)
- Set `home: true` on your home city to highlight it with a blue border
- Set `bg` to a hex colour or CSS gradient string to pre-set a card colour

---

## Built with

- Vanilla HTML, CSS, JavaScript
- No external libraries or frameworks
- SVG icons drawn inline

---

## About

Built by Elsa Frank as a portfolio project — a practical tool to track time across global teams, designed with a focus on clean UI and user experience.

Designed and developed with the help of Claude (Anthropic).
