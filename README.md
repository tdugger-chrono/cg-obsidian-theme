# CG Theme

A Chronograph-inspired theme for [Obsidian](https://obsidian.md). Brings the Chronograph app's look — clean white canvas, muted teal accent, near-black ink — into your notes, with a matching "CG dark" mode built on Chronograph's charcoal nav color.

The palette and typography come straight from the Chronograph codebase (`cg-web`): the UI accent teal (`#31828d`, Chrono Green darken-1), the deeper heading teal (`#0c7e84`), the grey ramp, and the **Open Sans** body/UI font.

> In Obsidian this theme appears as **cg obsidian theme** (the `name` in `manifest.json`).

| Mode | Look |
|---|---|
| Light | White canvas, `#31828d` teal accent, `#161b1a` ink — mirrors the app |
| Dark | `#272e2e` charcoal surfaces (the app's nav color), brighter teal for contrast |

## Fonts

The theme loads **Open Sans** from Google Fonts via `@import` to match Chronograph. This needs network access on first load; a fully offline vault falls back to the system sans-serif. To bundle the font for offline use, add the `.woff2` files to the repo and swap the `@import` for a `@font-face` block.

## Install

This theme is shared internally and is **not** in the Obsidian community store. Two ways to install:

### Manual (copy the folder)

1. In your vault, open `.obsidian/themes/` and create a folder named `cg obsidian theme`.
2. Copy `manifest.json` and `theme.css` into it.
3. In Obsidian: **Settings → Appearance → Themes → Manage → select "cg obsidian theme"**.

### BRAT (auto-updating)

If you have the [BRAT](https://github.com/TfTHacker/obsidian42-brat) community plugin:

1. **BRAT → Add beta theme**.
2. Paste `https://github.com/tdugger-chrono/cg-obsidian-theme`.
3. BRAT installs it and keeps it updated when new versions are tagged.

## Develop

The theme is plain CSS — no build step.

- Edit `theme.css`.
- Use the **Hot Reload** plugin to see changes live; otherwise `Cmd/Ctrl+R` reloads Obsidian.
- Colors use Obsidian's [CSS variables](https://docs.obsidian.md/Reference/CSS+variables/CSS+variables), scoped under `body.theme-light` and `body.theme-dark`; fonts use `--font-text-theme` / `--font-interface-theme`.

To cut a release for BRAT, bump `version` in `manifest.json` and tag the commit (`git tag 1.0.1 && git push --tags`).

## License

MIT — see [LICENSE](LICENSE).
