# EmuCoreH-Covers

Universal high-definition game cover repository for **EmuCoreH** and **Flycast**.

## Sega cartridge and CD systems

The 2026-10-23 IGDB refresh adds 2,042 cover sets, each with a flat JPEG and transparent 800×800 dark/light WebP case variants:

| Platform | Folder | Cover sets |
| --- | --- | ---: |
| Mega Drive / Genesis | `genesis/` | 1,118 |
| Sega CD / Mega-CD | `sega_cd/` | 198 |
| Sega 32X | `32x/` | 39 |
| Master System | `master_system/` | 341 |
| Game Gear | `game_gear/` | 245 |
| SG-1000 | `sg_1000/` | 101 |

Files use the IGDB game ID within the platform folder. For example, `genesis/<id>.jpg`, `genesis/3d/<id>.webp`, and `genesis/3d/light/<id>.webp`. The shared `index.json` preserves every existing Dreamcast title, serial and arcade mapping; new lookups live under `platforms[platformName]`. `sega_index.json` is the same platform-scoped subset. A game released on several systems has an entry in each applicable platform section, without replacing another system's mapping.

Flat images and metadata come from [IGDB](https://www.igdb.com/) through its [official API](https://api-docs.igdb.com/); each game record retains its source image URL and flat-image SHA-256. Covers are only mapped when source art exists. The case variants are stylized renders, with system-specific labels and colors. Sega CD follows the scan's aspect ratio for jewel-case or longbox artwork, preserving the complete front image. These renders do not claim to reproduce every regional packaging variation. Existing Dreamcast and arcade artwork is unchanged.

## Content
- **Dreamcast Covers (`covers/`)**: 1,085 covers upscaled to 2x resolution with Lanczos + UnsharpMask sharpening & contrast enhancement
- **Arcade Covers (`arcade/`)**: 253 arcade covers upscaled to 2x resolution with Lanczos + UnsharpMask sharpening
- **3D Box Art (`covers/3d/` & `covers/3d/light/`)**: 1,085 Dreamcast 3D jewel cases (Dark & Light themes) with centered game title spines (Segoe UI Bold) and zero diagonal plastic glare
- **3D Arcade Box Art (`arcade/3d/` & `arcade/3d/light/`)**: 253 Arcade 3D cases (Dark & Light themes) featuring arcade marquee headers, insert-coin footers, stylized wide-tracking spines (`NAOMI`, `NAOMI 2`, `ATOMISWAVE`, `SYSTEM SP`), uncropped 4:3 art, and zero ambient blur
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

The index contains 1,085 games, 863 title keys, 732 serial keys and 355 arcade keys: 253 direct artworks plus 102 reviewed revision/component fallbacks. Every target has flat, dark 3D and light 3D files. All 353 entries in the app's current arcade catalog have artwork; two additional artworks are `force five` and `kenju`. Two-character titles (`D2`, `Es`) and the exact aliases `toy story 2` and `shenmue 2` are included without merging regions, sequels or special editions.

Arcade artwork comes from [Flycast content](https://github.com/flyinghead/flycast-content/tree/master/arcade/jpg). The nine restored sets (`gundmgd`, `gundmxgd`, `slashout`, `vstrik3`, `vtennis2`, `vtennisg`, `wccf234j`, `wccf310j`, `wccf322e`) use the official [Flycast artwork site](https://flyinghead.github.io/flycast-content/arcade/jpg/), the same 2x flat-image processing and existing dark/light 3D renderer as the other covers.

## Additional arcade artwork

All 42 previously missing catalog entries are covered by 24 distinct artwork sets and 18 revision/component aliases. The curated flat images use horizontal 4:3 artwork at 1280x960, filling the entire image area. Dark and light 3D versions use the existing transparent 800x800 case renderer, geometry, scale and platform branding. Portrait flyers, camera photographs of cabinets or screens, and generic NAOMI error/boot placeholders are excluded.

The batch contains 18 digital game title/gameplay images and two existing Cycraft title screens. Wide publisher race images use an undistorted 4:3 race-scene viewport. World Edition and World Edition EX remain separate. Derby 2000 and II title screens identify their respective game families; they do not claim to show the Ver.2 / Ver.2.1 update number.

Anpanman Popcorn Factory 2 and SWP Hopper Board use custom digital title cards with their exact names, approved for cases without suitable digital game art. Heat Up Hockey Image and StarHorse Progress Returns use original, unmodified publisher logo pixels on designed graphic backgrounds. These four graphic covers are designed artwork, not official game screenshots. Their backgrounds/title-card illustrations were created with image generation. No photographic source is included.

| Artwork | Source / identity reference |
| --- | --- |
| Brick People / Block PeePoo (`brickppl`) | [genuine 4:3 arcade game title screen](https://gamesdb.launchbox-app.com/games/images/371459-brick-people) |
| Bingo Galaxy (main) (`bingogal`) | [official native landscape gameplay screenshot](https://www.sega.jp/history/arcade/product/7994/) |
| Galileo Factory (main) (`galilfac`) | [Genuine 4:3 gameplay screenshot with game logo](https://www.arcade-history.com/?id=29988&n=galileo-factory&page=detail) |
| Monopoly the Medal 2nd Edition (`monomedal`) | [Genuine 4:3 gameplay screenshot](https://www.arcade-history.com/?id=70945&n=monopoly-the-medal-2nd-edition&page=detail) |
| Dragon Treasure (Rev B) (`dragntr`) | [actual full landscape game title screenshot](https://gamesdb.launchbox-app.com/games/images/102339-dragon-treasure) |
| Dragon Treasure 2 (Rev A) (`dragntr2`) | [actual full landscape game title screenshot](https://gamesdb.launchbox-app.com/games/images/102340-dragon-treasure-ii) |
| Dragon Treasure 3 (Rev A) (`dragntr3`) | [actual full landscape game title screenshot](https://gamesdb.launchbox-app.com/games/images/102345-dragon-treasure-iii) |
| Sega Yonin Uchi Mahjong MJ (Update Disc Ver.1.008, Japan) (CDP-10002B) (`mj1`) | [original 2002 MJ landscape gameplay screenshot](https://gamesdb.launchbox-app.com/games/images/236736-sega-yonin-uchi-mahjong-mj) |
| Oinori-daimyoujin Matsuri (`oinori`) | [actual native full4:3 Matsuri gameplay screenshot](https://db.hfsplay.fr/games/78851-oinori-daimyoujin-matsuri?lang=en) |
| Derby Owners Club (Japan, Rev B) (`derbyoc`) | [actual game title screenshot](https://www.arcade-history.com/game/4139/derby-owners-club) |
| Derby Owners Club 2000 Ver.2 (Japan, Rev A) (`derbyo2k`) | [actual game title screenshot](https://www.arcade-history.com/game/37093/derby-owners-club-2000) |
| Derby Owners Club II Ver.2.1 (Japan, Rev B) (`derbyoc2`) | [actual dual-screen game title/program capture](https://www.arcade-history.com/game/31764/derby-owners-club-ii) |
| Derby Owners Club World Edition (Rev A) (`drbyocwa`) | [native digital game title screenshot](https://gamesdb.launchbox-app.com/games/images/35884-derby-owners-club-world-edition) |
| Derby Owners Club World Edition EX (Rev D) (`derbyocw`) | [actual game title screenshot](https://gamesdb.launchbox-app.com/games/images/137244-derby-owners-club-world-edition-ex) |
| Star Horse (satellite) (`shorse`) | [official Sega landscape gameplay screenshot](https://www.sega.jp/history/arcade/product/8929/) |
| Star Horse 2001 (satellite, Rev B) (`shors2k1`) | [official Sega landscape gameplay screenshot](https://www.sega.jp/history/arcade/product/8117/) |
| Star Horse 2002 (sound, Export/Taiwan) (`shors2k2`) | [official Sega landscape gameplay screenshot](https://www.sega.jp/history/arcade/product/8101/) |
| Star Horse Progress (satellite, Rev A) (`shorsep`) | [official Sega landscape gameplay screenshot](https://www.sega.jp/history/arcade/product/8837/) |
| Soreike! Anpanman Popcorn Koujou 2 (`anpanman2`) | [custom digital title card](https://www.am-j.co.jp/newmachine/200210/013.html) |
| SWP Hopper Board (`hopper`) | [custom digital title card](https://arcade.vastheman.com/minimaws/machine/hopper) |
| Heat Up Hockey Image (`huhimage`) | [official publisher digital logo on designed background](https://www.sega.jp/history/arcade/product/7308/) |
| Star Horse Progress Returns (satellite) (`shorsepr`) | [official publisher digital logo on designed background](https://www.sega.jp/history/arcade/product/15045/) |
| Club Kart for Cycraft (`clubkcyc`) | [Digital title screen](https://gamesdb.launchbox-app.com/games/images/35582-club-kart-for-cycraft) |
| Initial D Version 3 for Cycraft (`inidv3cy`) | [Digital title screen](https://gamesdb.launchbox-app.com/games/images/137246-initial-d-arcade-stage-ver-3-cycraft-edition) |

`hopper` is a service controller rather than a standalone game. `wccf1dup` is the WCCF 2001-2002 DIMM firmware updater and shares that season's existing title artwork. Tools, raw research files and working graphics stay outside the tracked artwork repository.
