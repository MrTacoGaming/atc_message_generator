# Automated ATC Script Generator

A responsive, client-side web tool built to automatically compile flight simulator radio transcripts. It parses structured user templates, identifies variable placeholders, dynamically builds input forms, and separates transmissions into highly distinct **Pilot** and **ATC** dialogue layouts.

## Live Demo
The application is deployed and hosted live on GitHub Pages.
* **Live Link:** `https://<YOUR-GITHUB-USERNAME>.github.io/<YOUR-REPO-NAME>/`

---

## Features

* **Dynamic Form Generator:** Automatically scans templates for bracketed variables `{like_this}` and generates individual clean text fields instantly.
* **Visual Conversation Stripping:** Splits text blocks automatically. Pilot messages feature an **emerald indicator** line, while Controller (ATC) responses use an **amber aviation text** block with a sky-blue accent.
* **Phase-of-Flight Presets:** Pre-configured with exact multi-line dialogue patterns mapped directly from flight coordination documentation:
  1. Clearance Delivery
  2. Pushback & Taxi
  3. Takeoff / Departure
  4. Climb / Cruise
  5. Descent / Approach
  6. Landing / Arrival
* **Persistent Browser Cache:** Utilizes the HTML5 `localStorage` API to securely save variables inside your browser so your active data isn't lost if you refresh or switch phases.
* **One-Click Utilities:** Quick-action layout modifications including a total data reset button and automated clipboard multi-line exports.

---

## 💻 Local Configuration & Setup

Since the system runs entirely on client-side native browser technologies, you do not need to install any external build frameworks, runtimes, or database servers.

### Prerequisites
* A standard modern web browser (Google Chrome, Mozilla Firefox, Microsoft Edge, or Apple Safari).
* A text editor (such as VS Code, Notepad++, or Sublime Text).

### Execution Steps
1. Clone the project locally onto your workstation machine:
   ```bash
   git clone https://github.com<YOUR-GITHUB-USERNAME>/<YOUR-REPO-NAME>.git
   ```
2. Enter the source folder:
   ```bash
   cd <YOUR-REPO-NAME>
   ```
3. Open the main file using your favorite operating system launcher shortcut:
   * **Windows:** Double-click `index.html` or type `start index.html` in your command line terminal.
   * **Mac:** Type `open index.html` in your terminal shell.
   * **Linux:** Type `xdg-open index.html` in your bash session window.

---

## 🤝 Production Publishing Roadmap

To publish adjustments directly to your live environment, push modifications into your tracking main branch:

```bash
git add .
git commit -m "Optimize responsive padding across standard display sizes"
git push origin main
```

*Note: Allow approximately 30 to 90 seconds after pushing for GitHub Actions to completely build and cascade the adjustments live to your active Pages instance.*

