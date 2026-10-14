# EmuCoreH-Covers

Universal high-definition game cover repository for **EmuCoreH** and **Flycast**.

## Content
- **Dreamcast Covers (`covers/`)**: 1,085 covers upscaled to 2x resolution with Lanczos + UnsharpMask sharpening & contrast enhancement
- **Arcade Covers (`arcade/`)**: 220 arcade covers upscaled to 2x resolution with Lanczos + UnsharpMask sharpening
- **3D Box Art (`covers/3d/` & `covers/3d/light/`)**: 1,085 Dreamcast 3D jewel cases (Dark & Light themes) with centered game title spines (Segoe UI Bold) and zero diagonal plastic glare
- **3D Arcade Box Art (`arcade/3d/` & `arcade/3d/light/`)**: 220 Arcade 3D cases (Dark & Light themes) featuring arcade marquee headers, insert-coin footers, stylized wide-tracking spines (`NAOMI`, `NAOMI 2`, `ATOMISWAVE`, `SYSTEM SP`), uncropped 4:3 art, and zero ambient blur
- **Index (`index.json` & `index.min.json`)**: Complete mapping of disc UIDs/product codes, titles, and arcade romsets

## Lookup Structure
- Direct Arcade (Flat): `arcade/<romset>.jpg`
- Direct Arcade (3D Dark): `arcade/3d/<romset>.webp`
- Direct Arcade (3D Light): `arcade/3d/light/<romset>.webp`
- Direct Dreamcast (Flat): `covers/<tgdb_id>.jpg`
- Direct Dreamcast (3D Dark): `covers/3d/<tgdb_id>.webp`
- Direct Dreamcast (3D Light): `covers/3d/light/<tgdb_id>.webp`
- Mapping: `index.json` maps `serials` (e.g. `MK51037`, `T1202N`), `titles`, and `arcade` romsets to their cover files.
