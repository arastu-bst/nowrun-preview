# nowrun player assets

Visual reference: the design page (six screens, today vs proposed, and the change list).
This folder is the spec that goes with it. Copy files into the repo; do not hot-link.

| file | use |
|---|---|
| `screens.css` | Styles for the six proposed screens. Same values the page renders. |
| `strings.md` | Every string on those screens, against the locale key it replaces. |
| `nowrun-wordmark.svg` | Wordmark, outlined from Geist. No font dependency. |
| `nowrun-app-placeholder.svg` | Fallback app tile. Boot animation is inside the file; works as a plain `<img>`. Only for APKs with no icon — the icon should be extracted on deploy. |
| `preloader-bg-light.png` | `uiConfig.customPreloader.backgroundUrl`. Flat colour because that slot stretches the image. |
| `preloader-bg-dark.png` | Same, dark, if ever wanted. |
| `og-1200x630.png` | Replaces `OG_Image.jpg` as the share preview. |
