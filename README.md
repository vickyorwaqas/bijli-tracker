# Bijli Tracker

Offline-first PWA for Pakistan: track your load shedding schedule and your electricity, gas and water bills. No backend, no build step, no dependencies. All data stays in your browser (IndexedDB).

## Features
- Live "power is on/off" status with countdown to the next cut (handles slots that cross midnight)
- Weekly schedule with per-day slots
- Reminders before a cut (Notification API + service worker)
- Bill log in PKR with units and per-unit rate, 6-month stacked chart, month-over-month change
- JSON export/import backup
- Installable, works fully offline

## Run
Service workers need http(s), so serve the folder:

    python3 -m http.server 8080

Open http://localhost:8080. To deploy, push to GitHub and enable Pages.

## Limits
Reminders fire only while the app is open or alive in the background. True push when the app is closed needs a push server, which this project deliberately avoids.

## License
MIT
