# CG Theme

A Chronograph-inspired theme for [Obsidian](https://obsidian.md). Brings the Chronograph app's look — clean white canvas, teal accent, near-black ink — into your notes, with a matching "CG dark" mode.

The palette is taken straight from the Chronograph codebase (`cg-web`), so the accent teal (`#11a8b2`, "Chrono Green"), heading teal (`#0c7e84`), and grey ramp match the product.

| | |
|---|---|
| Light | White canvas, teal accent, `#161b1a` ink — mirrors the app |
| Dark | CG ink (`#161b1a`) surfaces, brighter teal accent for contrast |

## Install

This theme is shared internally and is **not** in the Obsidian community store. Two ways to install:

### Manual (copy the folder)

1. In your vault, open `.obsidian/themes/` and create a folder named `CG Theme`.
2. Copy `manifest.json` and `theme.css` into it.
3. In Obsidian: **Settings → Appearance → Themes → Manage → select "CG Theme"**.

### BRAT (auto-updating)

If you have the [BRAT](https://github.com/TfTHacker/obsidian42-brat) community plugin:

1. **BRAT → Add beta theme**.
2. Paste `https://github.com/tdugger-chrono/cg-obsidian-theme`.
3. BRAT installs it and keeps it updated when new versions are tagged.

## Develop

The theme is plain CSS — no build step.

- Edit `theme.css`.
- In Obsidian, enable a reload or use the **Hot Reload** plugin to see changes live; otherwise `Cmd/Ctrl+R` reloads the app.
- Colors are driven by Obsidian's [CSS variables](https://docs.obsidian.md/Reference/CSS+variables/CSS+variables), scoped under `body.theme-light` and `body.theme-dark`.

To cut a release for BRAT, bump `version` in `manifest.json` and tag the commit (`git tag 1.0.1 && git push --tags`).

## License

MIT — see [LICENSE](LICENSE).
