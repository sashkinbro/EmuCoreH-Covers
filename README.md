# EmuCoreH-Covers

Universal game cover repository for **EmuCoreH** and **Flycast**.

## Content
- **Dreamcast Covers (`covers/`)**: 1085 game covers scraped from TheGamesDB
- **Arcade Covers (`arcade/`)**: 311 arcade covers from official Flycast repository
- **Index (`index.json`)**: Complete mapping of disc UIDs/product codes, titles, and arcade romsets

## Lookup Structure
- Direct Arcade: `arcade/<romset>.jpg`
- Direct Dreamcast: `covers/<tgdb_id>.jpg`
- Mapping: `index.json` maps `serials` (e.g. `MK51037`, `T1202N`) and `titles` to their cover files.
