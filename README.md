# EmuCoreH-Covers

Universal high-definition game cover repository for **EmuCoreH** and **Flycast**.

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

The remaining 42 catalog entries use 24 newly sourced cover sets and 18 reviewed aliases. Original flyers and title screens identify the correct game families; program revisions and system-component ROMs share that game's art. Derby World Edition and World Edition EX, and all five StarHorse generations, remain separate. Derby 2000 and II flyers identify the respective games but do not claim to depict the Ver.2 / Ver.2.1 software updates specifically.

Flat files are RGB JPEG at 1280x960 or 960x1280, with complete source art preserved. Dark and light 3D files use the same existing renderer, platform branding, transparent 800x800 canvas, box scale and margins as the rest of the repository. The Anpanman flyer photograph was perspective-corrected to the paper edges; no game art or text was redrawn.

| Artwork | Verified source |
| --- | --- |
| Bingo Galaxy (main) (`bingogal`) | [original Sega Japanese arcade flyer](https://www.sega.jp/history/arcade/product/7994/) |
| Galileo Factory (main) (`galilfac`) | [original Sega Japanese arcade flyer](https://www.sega.jp/history/arcade/product/7988/) |
| Monopoly the Medal 2nd Edition (`monomedal`) | [original Sega Japanese arcade flyer](https://www.sega.jp/history/arcade/product/7340/) |
| Heat Up Hockey Image (`huhimage`) | [original Sega Japanese arcade flyer](https://www.sega.jp/history/arcade/product/7308/) |
| Brick People / Block PeePoo (`brickppl`) | [original Sega English arcade flyer front](https://gamesdb.launchbox-app.com/games/images/371459-brick-people) |
| Dragon Treasure (Rev B) (`dragntr`) | [official promotional flyer front](https://www.sega.jp/history/arcade/product/8843/) |
| Dragon Treasure 2 (Rev A) (`dragntr2`) | [official promotional flyer front](https://www.sega.jp/history/arcade/product/7361/) |
| Dragon Treasure 3 (Rev A) (`dragntr3`) | [official promotional flyer front](https://www.sega.jp/history/arcade/product/7348/) |
| Sega Yonin Uchi Mahjong MJ (Update Disc Ver.1.008, Japan) (CDP-10002B) (`mj1`) | [original 2002 promotional flyer front scan](https://gamesdb.launchbox-app.com/games/images/236736-sega-yonin-uchi-mahjong-mj) |
| Soreike! Anpanman Popcorn Koujou 2 (`anpanman2`) | [photograph of authentic promotional brochure front](https://auctions.yahoo.co.jp/jp/auction/f1232887100) |
| Oinori-daimyoujin Matsuri (`oinori`) | [authentic promotional flyer front scan](https://gamesdb.launchbox-app.com/games/images/37933-oinori-daimyoujin-matsuri) |
| Club Kart for Cycraft (Rev A) (`clubkcyc`) | [title screen](https://gamesdb.launchbox-app.com/games/images/35582-club-kart-for-cycraft) |
| Initial D Arcade Stage 3 Cycraft Edition (Rev B) (`inidv3cy`) | [title screen](https://gamesdb.launchbox-app.com/games/images/137246-initial-d-arcade-stage-ver-3-cycraft-edition) |
| SWP Hopper Board (`hopper`) | [exact hardware photo](https://adb.arcadeitalia.net/dettaglio_mame.php?game_name=hopper) |
| Derby Owners Club (Japan, Rev B) (`derbyoc`) | [real Sega promotional flyer scan](https://gamesdb.launchbox-app.com/games/images/130055-derby-owners-club) |
| Derby Owners Club 2000 Ver.2 (Japan, Rev A) (`derbyo2k`) | [real Sega promotional flyer scan](https://gamesdb.launchbox-app.com/games/images/35882-derby-owners-club-2000) |
| Derby Owners Club II Ver.2.1 (Japan, Rev B) (`derbyoc2`) | [real Sega/Hitmaker promotional flyer scan](https://gamesdb.launchbox-app.com/games/images/35883-derby-owners-club-ii) |
| Derby Owners Club World Edition (Rev A) (`drbyocwa`) | [real Sega sales flyer scan](https://flyers.arcade-museum.com/videogames/show/4796) |
| Derby Owners Club World Edition EX (Rev D) (`derbyocw`) | [real Sega promotional flyer scan](https://gamesdb.launchbox-app.com/games/images/137244-derby-owners-club-world-edition-ex) |
| Star Horse (satellite) (`shorse`) | [real Sega promotional flyer scan](https://gamesdb.launchbox-app.com/games/images/39133-star-horse) |
| Star Horse 2001 (satellite, Rev B) (`shors2k1`) | [real Sega promotional flyer scan](https://gamesdb.launchbox-app.com/games/images/237092-star-horse-2001) |
| Star Horse 2002 (sound, Export/Taiwan) (`shors2k2`) | [real Sega promotional flyer scan](https://gamesdb.launchbox-app.com/games/images/236369-star-horse-2002) |
| Star Horse Progress (satellite, Rev A) (`shorsep`) | [real Sega promotional flyer scan](https://gamesdb.launchbox-app.com/games/images/39134-star-horse-progress) |
| Star Horse Progress Returns (satellite) (`shorsepr`) | [real Sega promotional flyer scan](https://gamesdb.launchbox-app.com/games/images/39135-star-horse-progress-returns) |

`hopper` is a service controller, not a standalone game: its cover shows the actual SWP Hopper ROM board with the matching EPR-24083 chip label, also documented by [Citylan](https://citylan.it/index.php/SWP_Hopper_Board). `wccf1dup` is the WCCF 2001-2002 DIMM firmware updater, so it shares the corresponding WCCF 2001-2002 title art rather than borrowing a later football season's cover.
