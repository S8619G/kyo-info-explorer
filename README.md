# Kyo Info Explorer

**Local search tool for Kyocera technical manuals and admin guides.** Everything runs on the field technician's own PC — no internet connection required after install.

Ships preloaded with two Kyocera TASKalfa MZ Series guides so techs can try the search immediately. Users upload their own PDFs to add more.

---

## Download

Grab the latest Windows portable zip from the [**Releases page**](https://github.com/S8619G/kyo-info-explorer/releases/latest).

## Install (Windows)

1. **Extract** the zip somewhere convenient, e.g. `C:\Tools\Kyo Info Explorer`
2. **First time only:** double-click `Setup Icon (run once).bat`. Creates a proper Kyo Info Explorer shortcut with the Kyocera icon.
3. **Double-click the Kyo Info Explorer shortcut.** The browser opens at `http://127.0.0.1:5000` with the app loaded — no command window appears.
4. Drag the shortcut to your Desktop or pin to Taskbar for one-click access.

If the shortcut ever fails, `Start Kyo Info Explorer.bat` is a fallback that works the same way with a small minimized command window visible.

## What's preloaded

- TASKalfa MZ Series — Operation Guide (617 excerpts)
- TASKalfa MZ Series — Command Center RX User Guide (188 excerpts)

Covers MZ7500i/ci, MZ8500i/ci, MZ9500i/ci, and MZ10500i.

## Features

- Hybrid search (vector + keyword) with filter panel: product model, firmware, document type, tenant, confidentiality
- Original page viewer with print-single-page and print-range support
- Table of Contents view (for reading) and Individual Excerpts view (for inspection)
- Local SQLite storage — nothing leaves the PC
- Upload PDF, DOCX, TXT, or Markdown up to 150 MB

## Where your data lives

```
%LOCALAPPDATA%\KyoInfoExplorer\
  kyo.db          <- SQLite database
  pages\          <- rendered page images for the manual viewer
  server.log      <- rolling server log (crash diagnostics)
```

## Troubleshooting

See [`docs/troubleshooting.md`](docs/troubleshooting.md).

## Requirements

- Windows 10 or 11 (64-bit)
- ~500 MB free disk space
- Modern browser (Chrome, Edge, or Firefox)

## Version

Current: see [Releases](https://github.com/S8619G/kyo-info-explorer/releases).

---

*Field Technician Edition — internal tool.*
