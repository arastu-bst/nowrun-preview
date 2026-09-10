# nowrun player assets

Visual reference: `states.html` at the repo root (nine screens, today vs proposed, and the change list), and `launch-state.html` for the launch screen on its own.
This folder is the spec that goes with it. Copy files into the repo; do not hot-link.

| file | use |
|---|---|
| `screens.css` | Styles for the six proposed screens. Same values the page renders. |
| `strings.md` | Every string on those screens, against the locale key it replaces. |
| `nowrun-wordmark.svg` | Wordmark, outlined from Geist. No font dependency. |
| `nowrun-app-placeholder.svg` | Fallback app tile. Boot animation is inside the file; works as a plain `<img>`. Only for APKs with no icon — the icon should be extracted on deploy. |
| `preloader-bg-light.png` | `uiConfig.customPreloader.backgroundUrl`. Flat colour because that slot stretches the image. |
| `preloader-bg-dark.png` | Same, dark, if ever wanted. |
| `wallpaper-dark.png` | Default `media.*.banner`: the flat ground behind a running app. |
| `wallpaper-light.png` | Same, light. Only useful if the wrapper overlay is removed. |
| `og-1200x630.png` | Replaces `OG_Image.jpg` as the share preview. |
