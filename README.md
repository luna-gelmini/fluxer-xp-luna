# Windows XP Luna Theme for Fluxer

A custom CSS override that restyles the Fluxer chat client after the Windows XP "Luna" look: beige dialog faces, blue gradient title bars, bevelled buttons, Tahoma text and the classic green-hills wallpaper.

The whole theme is one file: `fluxer-xp-luna.css`.

## Installation

1. Open Fluxer.
2. Go to **User Settings → Look & Feel → Custom CSS Overrides**.
3. Paste the full contents of `fluxer-xp-luna.css` and save.

To remove the theme, clear the Custom CSS Overrides field again.

## What it changes

- **Palette and tokens.** The `:root` block defines a `--luna-*` palette (dialog face, Luna blue, title-bar gradient, close-button red, desktop blue, shadow and bevel colours) and then remaps Fluxer's own design tokens to it: backgrounds (`--background-primary`, `--background-secondary`, …), text colours, panel controls, hover and selection modifiers, transitions and fonts (`Tahoma, "Trebuchet MS", Verdana, Geneva, sans-serif`).
- **Bevels.** `--luna-outset` and `--luna-inset` hold the two-tone border colours that give XP controls their raised and sunken edges.
- **Component overrides.** Rules target Fluxer's CSS-module class names with partial matches such as `[class*="NativeTitlebar.module__titlebar"]`. Covered areas include the native title bar and its window buttons, the user area, member list items, the new-messages bar, switches, radio groups, toggle buttons, the scroll indicator, the voice call view, voice control bar and connection status pop-out, and the `.lk-participant-*` tiles shown during calls.
- **Wallpaper.** The desktop background is embedded in the file as a base64 JPEG (`--luna-bliss`, 1024×576), so the theme makes no external requests.
- **Reduced motion.** One rule respects `html.reduced-motion` for the voice connection pop-out.

## Customizing

Everything visual flows from the variables at the top of the file. Change `--luna-blue`, `--luna-face` or `--luna-caption` to recolour the theme, or replace the `--luna-bliss` data URI with your own `url(...)` to swap the wallpaper.

## Compatibility

The selectors depend on Fluxer's internal class names (`*.module__*`). A Fluxer update that renames a component can leave that part of the theme unstyled until the selector is updated. If something breaks, report which Fluxer version you are on and what looks wrong.

## Credits and legal

Windows, Windows XP and the Luna visual style are trademarks of Microsoft Corporation, and the embedded wallpaper is the Windows XP "Bliss" photograph, whose rights belong to Microsoft. This is an unofficial fan recreation for personal use and is not affiliated with or endorsed by Microsoft or the Fluxer project.

No license file is included for the CSS itself.
