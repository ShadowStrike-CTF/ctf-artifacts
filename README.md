# CTF Artifacts

Parsed artifact outputs from digital forensics CTF images — a reference library for competition and research.

Raw images are large and competition-gated. This repo contains what matters: the parsed outputs, timelines, and extracted evidence ready to query.

---

## Structure

```
ctf-artifacts/
├── MVS/
│   ├── 2023/
│   │   └── iPhone/
│   │       ├── timeline.csv
│   │       ├── messages.csv
│   │       ├── locations.csv
│   │       └── ...
│   ├── 2024/
│   │   └── iPhone/
│   ├── 2025/
│   │   └── iPhone/
│   └── 2026/
│       └── iPhone/
├── Cellebrite/
│   ├── 2023/
│   │   ├── Abe/
│   │   └── Felix/
│   ├── 2024/
│   │   ├── File1/
│   │   └── Otto/
│   └── 2025/
├── MSAB/
│   └── (portal-only — structure reserved)
└── _schema/
    └── README.md
```

---

## What's in each folder

Each device folder contains parsed artifact outputs in CSV and/or JSON:

| File | Contents |
|---|---|
| `timeline.csv` | Unified timeline — all timestamped events across all artifact types |
| `messages.csv` | SMS, iMessage, WhatsApp, Signal |
| `locations.csv` | GPS coordinates, significant locations, routined data |
| `photos.csv` | Photo metadata including EXIF and location |
| `calls.csv` | Call history |
| `contacts.csv` | Contacts |
| `browser.csv` | Safari/Chrome browser history |
| `wifi.csv` | Wi-Fi network connections |
| `apps.csv` | Installed applications |
| `notes.csv` | Notes |
| `calendar.csv` | Calendar events |
| `health.csv` | Health and activity data |
| `biome.csv` | Biome events (TextInputSession, AppIntents, KeyboardTokenFrequency) |

---

## Source images

| Competition | Year | Device | Image file | Notes |
|---|---|---|---|---|
| MVS | 2023 | iPhone | `00008101-0010541A1130001E_files_full-001.zip` | On Kingston E: |
| MVS | 2024 | iPhone | `00008110-000925383620A01E_files_full.zip` | On Kingston E: |
| MVS | 2025 | iPhone | `00008110-0008196A2299401E_files_full-001.zip` | On Kingston E: |
| MVS | 2026 | iPhone 14 Plus | `iPhone14Plus.zip` | On Kingston E: |
| Cellebrite | 2023 | Abe | `CellebriteCTF23_Abe_.zip` | MD5: E6AACE42D05F400889BC9B9BE31CEB46 |
| Cellebrite | 2023 | Felix | `CellebriteCTF23_Felix.zip` | MD5: 996A913B1301AB011CA7DD8CA93A9400 |
| Cellebrite | 2024 | File1 | `Cellebrite_CTF_File1.zip` | On Kingston E: |
| Cellebrite | 2024 | Otto | `CellebriteCTF24_Otto.zip` | On Kingston E: |
| Cellebrite | 2025 | TBC | TBC | Downloading |

All raw images stored on Kingston E: drive (`E:\CTF_Images\`). Zip password for Cellebrite: stored in Bitwarden.

---

## Timestamps

All timestamps normalised to **UTC** in format `YYYY-MM-DD HH:MM:SS.sss`.

Apple epoch offset applied where required (+978307200 seconds from Unix epoch).

---

## Parser

Artifacts parsed using [Nika](https://github.com/ShadowStrike-CTF/Niki) — part of the [Strategos Suite](https://github.com/ShadowStrike-CTF/Strategos).

---

## Related

- [ctf-writeups](https://github.com/ShadowStrike-CTF/ctf-writeups) — Challenge solutions and writeups
- [toolkit](https://github.com/ShadowStrike-CTF/toolkit) — Helper utilities and scripts
- [ShadowStrike-suite](https://github.com/ShadowStrike-CTF/ShadowStrike-suite) — Full product family

## Author

GitHub: [ShadowStrike-CTF](https://github.com/ShadowStrike-CTF)
