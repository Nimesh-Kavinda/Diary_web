# Developer Diary — Nimesh

A personal developer diary built from git commit history across 15 projects (September 2025 → March 2026).

## Structure

```
diary/
  2025-09.md     — September 2025
  2025-10.md     — October 2025
  2025-11.md     — November 2025
  2025-12.md     — December 2025
  2026-01.md     — January 2026
  2026-02.md     — February 2026
  2026-03.md     — March 2026
diary-data.json  — Structured data (days + weeks)
index.html — Interactive calendar viewer
README.md
```

## Projects Covered

| Project | Period |
|---|---|
| gLabs_automator | Sep 2025 |
| busy_books | Sep–Oct 2025 |
| HabbitTracker_V2 / Habbit Flow | Sep 2025, Feb–Mar 2026 |
| ProductHub | Nov–Dec 2025 |
| textToVideo | Dec 2025 |
| videoGen_ext | Dec 2025 |
| WearIt-extension | Dec 2025–Jan 2026 |
| ultimatewebscraper-landingpage | Jan 2026 |
| pnitrest-borad-image-downloader-with-react | Jan 2026 |
| pintrest-pin-data-anaystic-chrome-extension | Jan 2026 |
| gemini_watermark_remover | Jan 2026 |
| Gemini_Image_Site | Feb 2026 |
| x-devloper-api | Feb 2026 |
| reddit-api-development | Feb 2026 |
| gmail_exporter_ext | Mar 2026 |

## Using the Calendar

Serve the folder locally (required for `fetch()` to work):

```bash
# Python
python -m http.server 8080

# Node (npx)
npx serve .

# VS Code
Use the "Live Server" extension
```

Then open: `http://localhost:8080/index.html`

## Day Types (Colour Code)

| Colour | Meaning |
|---|---|
| Blue | Real work day with git commits |
| Green / dashed | AI-inferred day (no commits — tasks inferred from context) |
| Orange | Annual leave |
| Red | Public holiday |
| Grey | Weekend |
| Purple `W#` | Week summary end date |

## diary-data.json Schema

```json
{
  "meta": { "owner": "", "window_start": "YYYY-MM-DD", "window_end": "YYYY-MM-DD" },
  "days": [
    { "date": "YYYY-MM-DD", "project": "Name", "tasks": ["..."], "type": "work" },
    { "date": "YYYY-MM-DD", "type": "leave" },
    { "date": "YYYY-MM-DD", "holiday": "Name", "type": "holiday" },
    { "date": "YYYY-MM-DD", "project": "Name", "tasks": ["..."], "type": "generated" }
  ],
  "weeks": [
    { "week": "Week 1", "start": "YYYY-MM-DD", "end": "YYYY-MM-DD", "summary": "..." }
  ]
}
```
