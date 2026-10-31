# TOAC

Air Consumption Tracker for timed events. Observers log each participant's cylinder
pressure as they move between stations, then compare events, stations and participants.

- Per-participant starting station, with rotation that wraps around
- Live station timers, event clock, and lap tracking
- Reusable station presets and event comparison
- Light and dark themes

## Run it

It's a single static file. Open `index.html` in a browser, or host it with GitHub Pages
(Settings → Pages → Deploy from branch → `main` / root).

## Data storage

This version saves events in the browser's `localStorage`, so data stays on the device that
entered it and isn't shared between observers. The storage layer is the small `localDb()`
adapter near the bottom of `index.html` (collection/doc/add/get/set/delete/orderBy/onSnapshot).
To sync across devices, replace it with a backend that offers the same calls, such as Firebase Firestore.
