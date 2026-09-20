# EmuCoreH-Covers

Cover art used by the **EmuCoreH** Android emulator (Sega Dreamcast, Naomi, Naomi 2,
Atomiswave). The app downloads covers from this repository at runtime; the bundled
`catalog/dreamcast_covers.json` index maps product codes and titles to the files here.

## Layout

```
covers/<igdb-id>.jpg          flat IGDB cover art
covers/3d/<igdb-id>.webp      cover rendered in the Dreamcast jewel-case template
catalog/dreamcast_covers.json index consumed by the app
```

`dreamcast_covers.json`:

```json
{
  "serials": { "MK51035": "7860" },
  "titles":  { "sonic adventure": "7860" },
  "games": {
    "7860": {
      "path": "covers/7860.jpg",
      "source_url": "https://images.igdb.com/.../co5jac.jpg",
      "sha256": "...",
      "path_3d": "covers/3d/7860.webp",
      "sha256_3d": "..."
    }
  }
}
```

The app first tries the file from this repository and falls back to `source_url`
(the original IGDB artwork) when a file has not been uploaded yet.

## Regenerating

The catalogue and both cover sets are generated from the IGDB snapshot that ships
with the app (`IGDB/games.db`):

```
python tools/dreamcast_covers.py --export-2d --render-3d --index
```

The 3D template is an original Dreamcast-style jewel case: white insert, the
two-armed Dreamcast swirl and the platform line
"SEGA DREAMCAST • NAOMI • NAOMI 2 • ATOMISWAVE" — deliberately not a PlayStation
box. Nothing else in the app depends on the artwork; the index is verified with
SHA-256 checksums.
