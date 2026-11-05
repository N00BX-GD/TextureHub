# texturehub.json format

Put `texturehub.json` in your texture pack, in the same folder as `pack.json`.
It works for folder packs and ZIP packs.

## Toggle option (on/off)

```json
{
  "name": "My Pack",
  "creator": "You",
  "version": "1.0.0",
  "options": [
    {
      "id": "blue-buttons",
      "name": "Blue Buttons",
      "description": "Swaps the menu buttons to blue",
      "default": false,
      "preview": "previews/blue-buttons.png"
    }
  ]
}
```

Files for this option go in `options/blue-buttons/` (folder name = the option `id`).
They use the same file names as the textures they replace.

## Multi-choice option (pick one variant)

```json
{
  "id": "menu-theme",
  "type": "choice",
  "name": "Menu Theme",
  "description": "Pick the look of the main menu",
  "default": "dark",
  "choices": [
    { "id": "dark",  "name": "Dark",  "preview": "previews/menu-dark.png" },
    { "id": "light", "name": "Light", "preview": "previews/menu-light.png" },
    { "id": "stock", "name": "Stock", "files": [] }
  ]
}
```

Files for each variant go in `options/<option id>/<choice id>/`,
for example `options/menu-theme/dark/`.

## Fields

| Field | Where | Notes |
|-------|-------|-------|
| `id` | option, choice | Required. Must be unique inside its pack. |
| `name` | option, choice | Shown in the UI. Defaults to the `id`. |
| `description` | option | Shown in the info popup. |
| `default` | option | `true`/`false` for toggles, a choice `id` for choices. |
| `files` | option, choice | Folders inside the pack to copy. Missing = the default folder above. `[]` = no files. |
| `preview` | option, choice | Image path inside the pack (png/jpg, max 4 MB). A choice without its own `preview` uses the option's. |
| `type` | option | `"choice"` for multi-choice (also implied by having `choices`). |

## Notes

- A spritesheet png and its `.plist` must be in the option folder together.
- Changes apply after the player restarts Geometry Dash.
- Keep preview images outside the `options/` folders so they are not copied into the overlay.

**Note from me**

this shi ez af
