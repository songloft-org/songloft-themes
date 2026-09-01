# Songloft Themes

[English](#english) | [中文](#中文)

---

## 中文

社区主题包仓库，为 [Songloft](https://github.com/songloft-org/songloft) 音乐播放器提供可安装的 `.songloft-theme` 主题包。

### 可用主题

| 主题 | 作者 | 说明 |
|------|------|------|
| Liquid Glass | Songloft | 半透玻璃质感、星蓝点缀（配 Lynx Liquid Glass 表面） |
| Neon Night | Songloft | 紫蓝色霓虹风格暗色主题 |
| Sakura | Songloft | 粉色樱花暖色主题 |

### 如何使用

**方式一：在线安装（推荐）**

在 Songloft 客户端中：`设置 → 外观 → 主题包 → 在线主题`，点击安装即可。

**方式二：手动导入**

1. 下载 `themes/<主题名>/theme.songloft-theme` 文件
2. 在客户端中：`设置 → 外观 → 主题包 → 导入主题包`
3. 选择下载的 `.songloft-theme` 文件导入

### 制作主题

想制作自己的主题？请参阅 [主题包制作指南](https://songloft.hanxi.cc/theme-pack-guide)。

### 贡献主题

1. Fork 本仓库
2. 在 `themes/` 下创建你的主题目录（如 `themes/my-theme/`）
3. 添加 `theme.songloft-theme` 文件（JSON 格式，参考下方 [主题格式](#主题格式)）
4. 提交 PR — 合并后会自动更新 `index.json` 索引

### 主题格式

`.songloft-theme` 文件为 JSON 格式：

```json
{
  "schemaVersion": 1,
  "id": "作者名.主题名",
  "name": "主题显示名",
  "version": "1.0.0",
  "author": "作者名",
  "description": "简短描述",
  "light": {
    "seedColor": "#RRGGBB",
    "backgroundColor": "#RRGGBB",
    "surfaceColor": "#RRGGBB",
    "glassColor": "#RRGGBB"
  },
  "dark": {
    "seedColor": "#RRGGBB",
    "backgroundColor": "#RRGGBB",
    "surfaceColor": "#RRGGBB",
    "glassColor": "#RRGGBB"
  },
  "playerGradient": ["#RRGGBB", "#RRGGBB"],
  "cardRadius": 16,
  "controlRadius": 20,
  "navigationRadius": 18
}
```

#### 字段说明

| 字段 | 必填 | 说明 |
|------|------|------|
| `schemaVersion` | 是 | 固定为 `1` |
| `id` | 是 | 唯一 ID，格式 `作者.名称` |
| `name` | 是 | 显示名称 |
| `version` | 是 | 语义化版本号 |
| `author` | 否 | 作者名 |
| `description` | 否 | 简短描述 |
| `light` | 否 | 亮色模式配色 |
| `dark` | 否 | 暗色模式配色 |
| `seedColor` | 是（如有 light/dark 节） | Material 3 种子色，用于生成完整调色板 |
| `backgroundColor` | 否 | 覆盖背景色 |
| `surfaceColor` | 否 | 覆盖表面色 |
| `glassColor` | 否 | 玻璃装饰色（Lynx 液态玻璃 sheen），独立于 seedColor；缺省回落星蓝基线 |
| `playerGradient` | 否 | 全屏播放器渐变色，2 个十六进制颜色 |
| `cardRadius` | 否 | 卡片圆角半径（0-100） |
| `controlRadius` | 否 | 控件圆角半径（0-100） |
| `navigationRadius` | 否 | 导航指示器圆角半径（0-100） |

---

## English

Community theme packs for [Songloft](https://github.com/songloft-org/songloft) music player.

### Available Themes

| Theme | Author | Description |
|-------|--------|-------------|
| Liquid Glass | Songloft | A translucent glass theme with star-blue accents — pairs with the Lynx Liquid Glass surfaces |
| Neon Night | Songloft | A dark theme with purple and blue neon accents |
| Sakura | Songloft | A warm cherry-blossom theme with pink accents |

### How to Use

**Option 1: Online Install (Recommended)**

In the Songloft app: `Settings → Appearance → Theme Packs → Online Themes`, then tap Install.

**Option 2: Manual Import**

1. Download the `themes/<theme-name>/theme.songloft-theme` file
2. In the app: `Settings → Appearance → Theme Packs → Import`
3. Select the downloaded `.songloft-theme` file

### Create Your Own

See the [Theme Pack Development Guide](https://songloft.hanxi.cc/en/theme-pack-guide) for full details.

### Contributing

1. Fork this repository
2. Create a directory under `themes/` (e.g. `themes/my-theme/`)
3. Add a `theme.songloft-theme` file (JSON format, see [Theme Format](#theme-format) below)
4. Submit a PR — `index.json` will be updated on merge

### Theme Format

`.songloft-theme` files are JSON:

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
    "surfaceColor": "#RRGGBB",
    "glassColor": "#RRGGBB"
  },
  "dark": {
    "seedColor": "#RRGGBB",
    "backgroundColor": "#RRGGBB",
    "surfaceColor": "#RRGGBB",
    "glassColor": "#RRGGBB"
  },
  "playerGradient": ["#RRGGBB", "#RRGGBB"],
  "cardRadius": 16,
  "controlRadius": 20,
  "navigationRadius": 18
}
```

#### Fields

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
| `seedColor` | Yes (if light/dark present) | M3 seed color for palette generation |
| `backgroundColor` | No | Override background color |
| `surfaceColor` | No | Override surface color |
| `glassColor` | No | Glass decorative tint (Lynx Liquid Glass sheen), independent of seedColor; falls back to star-blue baseline when absent |
| `playerGradient` | No | Array of 2 hex colors for player gradient |
| `cardRadius` | No | Border radius for cards (0-100) |
| `controlRadius` | No | Border radius for controls (0-100) |
| `navigationRadius` | No | Border radius for navigation (0-100) |

## License

[Apache-2.0](LICENSE)
