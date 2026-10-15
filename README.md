# EmuCoreH-Covers

Universal high-definition game cover repository for **EmuCoreH** and **Flycast**.

## Content
- **Dreamcast Covers (`covers/`)**: 1,085 covers upscaled to 2x resolution with Lanczos + UnsharpMask sharpening & contrast enhancement
- **Arcade Covers (`arcade/`)**: 229 arcade covers upscaled to 2x resolution with Lanczos + UnsharpMask sharpening
- **3D Box Art (`covers/3d/` & `covers/3d/light/`)**: 1,085 Dreamcast 3D jewel cases (Dark & Light themes) with centered game title spines (Segoe UI Bold) and zero diagonal plastic glare
- **3D Arcade Box Art (`arcade/3d/` & `arcade/3d/light/`)**: 229 Arcade 3D cases (Dark & Light themes) featuring arcade marquee headers, insert-coin footers, stylized wide-tracking spines (`NAOMI`, `NAOMI 2`, `ATOMISWAVE`, `SYSTEM SP`), uncropped 4:3 art, and zero ambient blur
- **Index (`index.json` & `index.min.json`)**: Complete mapping of disc UIDs/product codes, titles, and arcade romsets

## Lookup Structure
- Direct Arcade (Flat): `arcade/<romset>.jpg`
- Direct Arcade (3D Dark): `arcade/3d/<romset>.webp`
- Direct Arcade (3D Light): `arcade/3d/light/<romset>.webp`
- Direct Dreamcast (Flat): `covers/<tgdb_id>.jpg`
- Direct Dreamcast (3D Dark): `covers/3d/<tgdb_id>.webp`
- Direct Dreamcast (3D Light): `covers/3d/light/<tgdb_id>.webp`
- Mapping: `index.json` maps `serials` (e.g. `MK51037`, `T1202N`), `titles`, and `arcade` romsets to their cover files.

## Index maintenance

The `games` metadata and existing regional title/serial defaults in `index.json` are maintained inputs. Preserve their current choices when keys collide; a new ambiguous key requires an explicit default. Reviewed exact title aliases and clone-to-parent artwork paths are recorded in `aliases.json`. A clone's own artwork takes priority when all three styles exist. Both indices must stay in sync, with exact path case, including `FORCE FIVE` and `KENJU`; `updated_at` changes only when catalog content changes. Local maintenance tools are excluded from this artwork repository.

The index contains 1,085 games, 863 title keys, 732 serial keys and 313 arcade keys: 229 direct artworks plus 84 reviewed clone fallbacks. Every target has flat, dark 3D and light 3D files. Against the app's current 353-entry arcade catalog, 311 entries have artwork and 42 still need artwork; two additional artworks are `force five` and `kenju`. Two-character titles (`D2`, `Es`) and the exact aliases `toy story 2` and `shenmue 2` are included without merging regions, sequels or special editions.

Arcade artwork comes from [Flycast content](https://github.com/flyinghead/flycast-content/tree/master/arcade/jpg). The nine restored sets (`gundmgd`, `gundmxgd`, `slashout`, `vstrik3`, `vtennis2`, `vtennisg`, `wccf234j`, `wccf310j`, `wccf322e`) use the official [Flycast artwork site](https://flyinghead.github.io/flycast-content/arcade/jpg/), the same 2x flat-image processing and existing dark/light 3D renderer as the other covers.
