# Songloft Themes

Community theme packs for [Songloft](https://github.com/songloft-org/songloft) music player.

## Available Themes

| Theme | Author | Description |
|-------|--------|-------------|
| Neon Night | Songloft | A dark theme with purple and blue neon accents |
| Sakura | Songloft | A warm cherry-blossom theme with pink accents |

## Contributing

1. Create a new directory under `themes/` with your theme name
2. Add a `theme.songloft-theme` file (JSON format, see [schema](#theme-format))
3. Submit a PR — the index will be updated on merge

## Theme Format

`.songloft-theme` files are JSON with the following structure:

```json
{
  "schemaVersion": 1,
  "id": "your-name.theme-name",
  "name": "Theme Name",
  "version": "1.0.0",
  "author": "Your Name",
  "description": "Short description",
  "light": {
    "seedColor": "#RRGGBB",
    "backgroundColor": "#RRGGBB",
    "surfaceColor": "#RRGGBB"
  },
  "dark": {
    "seedColor": "#RRGGBB",
    "backgroundColor": "#RRGGBB",
    "surfaceColor": "#RRGGBB"
  },
  "playerGradient": ["#RRGGBB", "#RRGGBB"],
  "cardRadius": 16,
  "controlRadius": 20,
  "navigationRadius": 18
}
```

### Fields

| Field | Required | Description |
|-------|----------|-------------|
| `schemaVersion` | Yes | Must be `1` |
| `id` | Yes | Unique ID in `author.name` format |
| `name` | Yes | Display name |
| `version` | Yes | Semantic version |
| `author` | No | Author name |
| `description` | No | Short description |
| `light` | No | Light mode colors |
| `dark` | No | Dark mode colors |
| `light.seedColor` / `dark.seedColor` | Yes (if section present) | M3 seed color for palette generation |
| `light.backgroundColor` / `dark.backgroundColor` | No | Override background color |
| `light.surfaceColor` / `dark.surfaceColor` | No | Override surface color |
| `playerGradient` | No | Array of 2 hex colors for full-screen player gradient |
| `cardRadius` | No | Border radius for cards (0-100) |
| `controlRadius` | No | Border radius for controls/inputs (0-100) |
| `navigationRadius` | No | Border radius for navigation indicators (0-100) |
