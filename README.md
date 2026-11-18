# Afterglow

A sleek, modern dark theme for [Vencord](https://vencord.dev): near-black graphite surfaces, hairline borders, soft rounded panels and a single cool emerald accent (emerald into teal) used only where it matters. Calm, quick motion and no visual noise.

![Version](https://img.shields.io/badge/version-1.1.0-2fd6a0) ![Vencord](https://img.shields.io/badge/client-Vencord-1fb5c9) ![Dark only](https://img.shields.io/badge/mode-dark-0a0b0d)

## Features

- **A fully themed palette.** Afterglow recolours Discord's base colour scales, not just a handful of surfaces. The neutral scale becomes a barely tinted graphite and the blurple scale becomes emerald, so buttons, toggles, radios, selected rows, highlights and hover states all follow the theme.
- **Restrained accent.** The emerald-to-teal gradient appears only where it carries meaning: the selected server pill, the selected channel tick, mention and reply bars, blockquote bars, brand buttons and focused inputs.
- **Quiet, layered surfaces.** Near-black backgrounds, hairline borders and soft rounded corners. The user panel, context menus and popouts float as frosted glass cards with a thin edge light.
- **Calm motion:**
  - Messages fade up as they arrive, and the message list fades in when you switch channels.
  - Context menus, popouts and modals pop open; tooltips fade up.
  - Server icons lift on hover and press in on click; reactions rise on hover.
  - Links get a gradient underline that sweeps in on hover.
  - The typing dots pick up the accent, and the settings cog turns on hover.
- **A faint corner glow.** A soft emerald and teal haze sits in two corners of the app frame. Set `--ag-haze` to `0` to turn it off.
- **Display typography.** The UI uses [Chakra Petch](https://fonts.google.com/specimen/Chakra+Petch), headings and labels use wide-tracked [Orbitron](https://fonts.google.com/specimen/Orbitron), and code uses [JetBrains Mono](https://www.jetbrains.com/lp/mono/).
- **Respects reduce motion.** If *Reduce Motion* is on in Discord or in your OS, every animation and hover movement turns off.
- **Works with every dark variant.** Dark, Darker and Midnight all pick up the theme. Nitro profile themes keep their own colours.

## Installation

### Option 1: Online theme (updates automatically)

1. Open Discord → **Settings** → **Vencord** → **Themes** → **Online Themes**.
2. Paste this link and save:

   ```
   https://raw.githubusercontent.com/MercenaryUSA/Afterglow/main/Afterglow.theme.css
   ```

### Option 2: Local file

1. Download [`Afterglow.theme.css`](Afterglow.theme.css).
2. Open Discord → **Settings** → **Vencord** → **Themes** → **Open Themes Folder**.
3. Drop the file in. On Windows the folder is `%APPDATA%\Vencord\themes`.
4. Enable **Afterglow** in the list.

Use Discord's **Dark** (or Darker / Midnight) appearance. Afterglow is dark-only.

## Customization

Every colour, size and timing is a variable in the first `:root` block of the file ("Knobs"). Edit them in your local copy, or override them in Vencord's **QuickCSS**:

```css
:root {
    --ag-accent: #7aa2ff;        /* main accent */
    --ag-accent-hsl: 223 100% 74%;
    --ag-accent-2: #b48cff;      /* second gradient colour */
    --ag-accent-strong: #3a5bc7; /* filled buttons, brand surfaces */
    --ag-accent-2-strong: #5b3fb0;
    --ag-haze: 0;                /* turn off the corner glow */
}
```

| Variable | What it controls |
|---|---|
| `--ag-accent`, `--ag-accent-2` | Accent colour and the second gradient colour |
| `--ag-accent-strong`, `--ag-accent-2-strong` | Darker accent shades for filled buttons and badges (kept dark enough for white text) |
| `--ag-bg-0` / `--ag-bg-1` / `--ag-bg-2` | App frame and server bar, chat, and channel sidebar backgrounds |
| `--ag-surface-1` / `-2` / `-3` | Cards, menus, tooltips and other raised surfaces |
| `--ag-text-strong` / `--ag-text` / `--ag-text-muted` / `--ag-text-subtle`, `--ag-link` | Text and link colours |
| `--ag-line-1` / `-2` / `-3`, `--ag-line-accent` | Hairline borders |
| `--ag-font`, `--ag-font-display`, `--ag-font-code` | UI font, heading font and code font |
| `--ag-radius-sm` / `-md` / `-lg` / `-pill` | Corner rounding |
| `--ag-haze` | Strength of the corner glow in the app frame (`0` turns it off) |
| `--ag-fast` / `--ag-med` / `--ag-slow`, `--ag-ease` | Animation speeds and easing curve |
| `--ag-glass`, `--ag-blur`, `--ag-edge`, `--ag-shadow`, `--ag-ring` | Glass fill and blur, edge light, drop shadow and focus ring |

Note that Discord's recoloured blurple scale (section 2 of the file) is built around hue `161`. If you move the accent to a very different hue, update that scale too, or some secondary highlights will stay green.

## Compatibility

- Built for the Discord desktop client with Vencord, against Discord's November 2026 build.
- Discord's CSS class names include build hashes, e.g. `message_SY_P2T`, and these can change when Discord updates. Colours and fonts use Discord's design tokens, so they keep working across updates. If a few effects stop showing up, the class names behind them probably changed. Please open an issue.
- Fonts load from Google Fonts, with jsdelivr as a fallback. If neither is reachable, Discord's default font is used.

## License

Free to use, modify and share. Credit is appreciated.
