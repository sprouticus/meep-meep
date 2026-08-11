# Meep Meep — NM Rail Runner

A mobile app prototype for the [New Mexico Rail Runner Express](https://www.riometro.org/), the commuter rail line running between Belen and Santa Fe.

**▶ [Live demo](https://sprouticus.github.io/meep-meep/)** — best viewed on a phone, or in a desktop browser (the prototype renders inside a phone frame).

---

## The problem

Checking when the next Rail Runner train leaves means opening a PDF timetable, finding your station in a grid of 15 stops, and doing the arithmetic yourself. Meep Meep answers the only question most riders actually have: *when is my next train, and when does it get me there?*

## What it does

- **Next-train hero card** with a live countdown to departure, plus arrival time at your destination
- **Tappable route bar** (`Belen → Santa Fe Depot`) that opens a bottom sheet to change direction or stations — secondary controls stay tucked away so the schedule owns the screen
- **Full day's departures** below the hero, with expandable rows showing every intermediate stop
- **Local / Express filter** in the departures header, sticky for the session
- **Pin "My Train"** to keep a chosen departure highlighted
- **Buy Tickets** link that routes to the right destination for the user's device
- All 15 stations, both directions

## Design notes

The palette is drawn from the New Mexico landscape — sand, adobe, and brown — with the Rail Runner's own red and yellow reserved for CTAs and live states. The layout borrows from weather apps: one dominant "right now" answer up top, detail underneath for people who want it.

Two decisions worth calling out:

- **No onboarding gate.** Early drafts opened with a station-picker flow. It was cut — the route bar is always editable, so the app can open straight to a usable default instead of asking questions first.
- **GPS is optional, not required.** Auto-detecting the nearest station is a convenience, not a dependency. The app works fully without location permission.

## Built with

Plain HTML, CSS, and JavaScript in a single file — no build step, no dependencies. Open `index.html` and it runs. The prototype locks to phone dimensions in a desktop browser so it can be shared as a link without losing the mobile framing.

## Status

This is a design prototype, not a production app.

- Schedule data is **synthetic and representative** — realistic in shape, but not the live timetable. Production would read the official GTFS feed.
- The intended end state is a native mobile app (React Native / Expo). This web prototype exists to iterate on the interaction design quickly.

## License

MIT
