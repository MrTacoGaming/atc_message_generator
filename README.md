# ATC Script Generator

A self-contained, client-side web tool for generating realistic ATC radio transcripts for Roblox flight simulators. Select a flight phase, fill in the variables, and get a formatted Pilot/ATC dialogue ready to copy or download — no server, no build step, no internet required.

**Live:** `https://mrtacogaming.github.io/atc_message_generator/`

---

## Features

- **6 Flight Phases** — Clearance, Pushback & Taxi, Takeoff, Cruise, Approach, Landing
- **Dynamic Form Generator** — scans templates for `{variable}` tokens and builds input fields automatically
- **Editable Airline Name** — replaces the callsign across all phase templates
- **Color-coded Transcript** — Pilot blocks (emerald) and ATC blocks (amber/sky) are visually distinct
- **Example Data** — one-click fill with a realistic EDDF → EGLL sample flight
- **Save Slots (A / B / C)** — save and reload full sessions from browser storage
- **Persistent Storage** — field values survive page refreshes via `localStorage`
- **Copy & Download** — copy transcript to clipboard (`Ctrl+Enter`) or download as `.txt`
- **Dark / Light Mode** — theme toggle persisted across sessions
- **Phase Progress Bar** — visual indicator of position in the 6-phase flow
- **Input Hints** — format guidance on key fields (squawk, frequencies, FL notation)
- **Zero Dependencies** — no CDN, no framework, no network required

---

## Running Locally

```bash
git clone https://github.com/MrTacoGaming/atc_message_generator.git
cd atc_message_generator
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

No install step needed. Open the file in any modern browser.

---

## Deploying

Push to `main` — GitHub Pages deploys automatically within ~60 seconds.

```bash
git add .
git commit -m "your message"
git push origin main
```
