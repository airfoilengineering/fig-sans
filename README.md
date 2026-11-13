# Fig Sans

Fig Sans is the typeface Airfoil designed for Fig. This repository is the source of truth for the font: it holds the released font files, the design sources they are built from, and notes on how to install and use them.

## What is where

| Path | What it holds |
| --- | --- |
| `fonts/otf/` | OpenType (CFF) desktop fonts, for design tools and print |
| `fonts/ttf/` | TrueType desktop fonts, for Windows and app bundles |
| `fonts/web/` | WOFF2 and WOFF web fonts |
| `sources/` | Design sources (Glyphs or UFO) the font files are built from |
| `CHANGELOG.md` | What changed in each release |
| `LICENSE.md` | Terms of use |

Font files are named `FigSans-<Style>.<ext>`, for example `FigSans-Regular.otf` or `FigSans-BoldItalic.woff2`.

## Installing

**Desktop.** Download the latest release, or clone this repository, and install the files in `fonts/otf/`. On macOS, open a file and choose Install, or drag it into Font Book. On Windows, right-click a file and choose Install.

**Web.** Copy the files in `fonts/web/` into your project and declare each style with `@font-face`:

```css
@font-face {
  font-family: "Fig Sans";
  src: url("/fonts/FigSans-Regular.woff2") format("woff2"),
       url("/fonts/FigSans-Regular.woff") format("woff");
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

body {
  font-family: "Fig Sans", system-ui, sans-serif;
}
```

Repeat the block for each weight and style, changing `font-weight` and `font-style` to match.

## Releases

Every release is tagged `vMAJOR.MINOR.PATCH` and carries the same version number as the font files. Download font files from the Releases page rather than from a branch, so you always get a build that has been checked.

## Updating the font

1. Make the change in `sources/`.
2. Export new font files into `fonts/`, replacing the old ones. Keep the file names the same.
3. Bump the version in the sources and describe the change in `CHANGELOG.md`.
4. Open a pull request. Once it is merged, tag the release.

## Ownership

Fig Sans was designed by Airfoil for Fig. See `LICENSE.md` for the terms of use.
