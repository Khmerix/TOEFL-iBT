# TOEFL-iBT

A browser-based **TOEFL iBT mock test platform** built with HTML and CSS. The project provides a complete test-style experience with Reading, Listening, Speaking, and Writing sections, plus a styled dashboard, timers, progress tracking, and section-specific interactions.

## Live Demo

The site is published with GitHub Pages:

**https://khmerix.github.io/TOEFL-iBT/**

## Overview

This repository contains a front-end TOEFL practice environment designed to simulate a full test flow:

- Student login screen
- Security notice and anti-cheating warning flow
- Dashboard for selecting sections
- Reading section
- Listening section with audio assets
- Speaking section with microphone recording support
- Writing section with sentence-building and written responses

The main entry point is `index.html`, which combines the full experience into one interface.

## Features

- **Full mock test flow** from login to submission
- **Four TOEFL sections**: Reading, Listening, Speaking, and Writing
- **Progress tracking** across sections
- **Built-in timers** for timed test behavior
- **Listening audio playback** using bundled MP3 files
- **Speaking recording** using the browser microphone API
- **Writing activities** including sentence building and free-text responses
- **Section-based visual design system** with shared CSS files
- **Security monitoring UI** for tab switching / warning overlays
- **GitHub Pages deployment** for easy hosting

## Project Structure

```text
TOEFL-iBT/
├── index.html
├── toefl-styles.css
├── toefl-section-colors.css
├── TEMPLATE.html
├── toeflreading-MIGRATED.html
├── toefllistening-MIGRATED.html
├── toeflspeaking-MIGRATED.html
├── toeflwriting-MIGRATED.html
├── listening/
│   ├── toefllistening-MIGRATED.html
│   ├── *.mp3
│   ├── start-server.bat
│   └── start-server.ps1
├── Speaking/
│   ├── toeflspeaking-MIGRATED.html
│   ├── *.mp3
│   ├── google-apps-script-code.gs
│   └── SETUP-GOOGLE-DRIVE.md
├── DESIGN-SYSTEM.md
├── README-DESIGN-SYSTEM.md
├── MIGRATION-GUIDE.md
├── MIGRATION-COMPARISON.md
└── REPAIR-REPORT.md
```

## Key Files

- `index.html` — main all-in-one TOEFL test application
- `toefl-styles.css` — shared UI styles and reusable components
- `toefl-section-colors.css` — color themes for Reading, Listening, Speaking, and Writing
- `TEMPLATE.html` — starter template for building additional sections/pages
- `listening/` — listening section HTML and audio files
- `Speaking/` — speaking section assets, audio prompts, and optional Google Apps Script integration

## Running Locally

Because this project is mostly static HTML/CSS, you can run it in a browser directly.

### Option 1: Open directly

Open `index.html` in your browser.

### Option 2: Use a local server

A local server is recommended for testing media behavior more reliably.

Examples:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

The `listening/` folder also includes helper scripts for starting a local server on Windows:

- `start-server.bat`
- `start-server.ps1`

## Section Notes

### Reading
- Presented inside the main test flow
- Includes timed reading activity and question interface

### Listening
- Uses bundled MP3 files stored in `listening/`
- Simulates TOEFL-style listening prompts and question groups

### Speaking
- Uses `navigator.mediaDevices.getUserMedia(...)` and `MediaRecorder` in the browser
- Includes prompt playback and recorded response flow
- Recording duration differs by task type
- Repository also includes optional Google Drive upload setup in `Speaking/google-apps-script-code.gs` and `Speaking/SETUP-GOOGLE-DRIVE.md`

### Writing
- Includes sentence arrangement activities
- Includes text areas with word counting behavior
- Tracks progress across writing tasks

## Design System

This repository also includes design-system and migration documentation:

- `DESIGN-SYSTEM.md`
- `README-DESIGN-SYSTEM.md`
- `MIGRATION-GUIDE.md`
- `MIGRATION-COMPARISON.md`

These files document the shared component styles, section color themes, and migration work for the updated TOEFL UI.

## Speaking Upload Integration

The `Speaking/` directory includes optional Google Apps Script code for uploading speaking recordings to Google Drive:

- `google-apps-script-code.gs`
- `SETUP-GOOGLE-DRIVE.md`

This is useful if you want recorded speaking responses to be stored externally instead of only handled in-browser.

## Tech Stack

- **HTML**
- **CSS**
- **Vanilla JavaScript**
- **Tailwind CSS via CDN**
- **Font Awesome**
- **Google Fonts**

## Use Cases

This project can be used for:

- TOEFL practice/mock exams
- Classroom test simulations
- UI prototyping for online testing systems
- Learning static front-end structure for quiz/test apps

## Notes

- This repository is primarily a **front-end prototype / static web app**.
- Some features, such as speaking upload workflows, may require additional setup if you want persistent storage.
- Microphone-based features require browser permission.

## License

No license file is currently defined in this repository.
