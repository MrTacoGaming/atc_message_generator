# ATC Script Generator

A self-contained, client-side web tool for generating realistic ATC radio transcripts for Roblox flight simulators. Select a flight phase, fill in the variables, and get a formatted Pilot/ATC dialogue ready to copy or download — no server, no build step, no internet required.

**Live:** `https://mrtacogaming.github.io/atc_message_generator/`

---

## Features

- **8 Flight Phases** — ATIS, Clearance, Pushback & Taxi, Takeoff, Departure, Cruise, Approach, Landing
- **Dynamic Form Generator** — scans templates for `{variable}` tokens and builds input fields automatically
- **Editable Airline Name** — replaces the callsign across all phase templates
- **Color-coded Transcript** — Pilot blocks (emerald) and ATC blocks (amber/sky) are visually distinct
- **Example Data** — one-click fill with a realistic EDDF → EGLL sample flight
- **Named Save Slots (A / B / C)** — save, label, and reload full sessions from browser storage
- **Export / Import Sessions** — round-trip your full state through a JSON file for backup or sharing
- **Random Value Generators** — 🎲 buttons fill squawk codes, VHF frequencies, and runways with realistic values
- **Input Validation** — amber warnings flag implausible squawks, frequencies, runways, altitudes, and wind values
- **Radio Static Toggle** — Web Audio synthesis adds an immersive crackle on phase change
- **Persistent Storage** — field values survive page refreshes via `localStorage`
- **Copy & Download** — copy transcript to clipboard (`Ctrl+Enter`) or download as `.txt`
- **Dark / Light Mode** — theme toggle persisted across sessions
- **Phase Progress Bar** — visual indicator of position in the 8-phase flow
- **Input Hints** — format guidance on key fields (squawk, frequencies, FL notation)
- **Zero Dependencies** — no CDN, no framework, no network required

---

## Changelog

### 2026-05-21

- Added ATIS phase (before Clearance) and Departure Control phase (between Takeoff and Cruise); progress bar now spans 8 phases.
- Added 🎲 random-value buttons for squawk codes (excluding 0000/7500/7600/7700/7777), VHF frequencies (118.000–136.975 MHz, 25 kHz steps), and runways (01–36 with optional L/C/R).
- Added input validation: fields with unrealistic values get an amber border and inline hint. Not a blocker — just a nudge towards realistic phraseology.
- Added named save slots: click the ✎ icon on a slot card to rename it. Custom names persist alongside the existing route summary fallback.
- Added Export / Import buttons in the Saved Sessions card. Exports airline, current values, all slots, slot labels, and theme to a JSON file; import asks for confirmation before overwriting.
- Added radio static audio toggle (header). Synthesizes a bandpass-filtered noise burst via the Web Audio API on phase change; preference persists in `localStorage`.

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
