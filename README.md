# Attune

A partner-side cycle companion. Most cycle apps are built for her; Attune is built for the person next to her — it explains what is happening in her body at each phase, what she is likely feeling, and how to show up for her.

Single-file, installable web app. No backend, no accounts, no analytics. Everything you log stays in `localStorage` on your own device.

## Install on your phone

Open the app in your phone's browser, then:

- **iPhone (Safari):** Share → Add to Home Screen
- **Android (Chrome):** menu (⋮) → Install app / Add to Home screen

It launches full-screen, works offline after the first load, and updates itself whenever you open it online.

## What it does

- **Today** — current phase, cycle day, what is happening hormonally, and the three most useful things you can do right now
- **Log** — record period starts and mood check-ins; each check-in explains whether the mood fits the phase and what to do or avoid
- **Map** — the whole cycle at a glance, with phase bands and her pain days marked
- **Tips** — the full support library, filterable by phase and category, every tip carrying its "why"
- **Settings** — cycle numbers, her name, her known patterns, and JSON export/import for backups

## Setup

The app opens on a neutral starting state. Two things make it yours:

1. **Log her last period start** — Log → Pick a date. Everything (phase, predictions, countdown) follows from that.
2. **Set her name** — Settings → Her name. Left blank, the whole app reads "her".

Her patterns (Settings) ship with a common starter set. Delete what does not apply and add what you learn.

## Files

Plain static files, no build step:

- `index.html` — the entire app: brush engine, cycle engine, content, and UI
- `manifest.json`, `sw.js` — PWA install + offline cache
- `icon-192.png`, `icon-512.png` — app icons

Serve the folder over http to develop:

```bash
python3 -m http.server 8093
```

## Not medical advice

Attune explains and suggests. It does not diagnose, and it is not a fertility or contraception tool. Anything severe or new is a reason to encourage a doctor's visit, not to consult an app.
