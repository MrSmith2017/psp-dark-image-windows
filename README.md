# PaintShop Pro Dark Image Windows

A [Windhawk](https://windhawk.net) mod that gives the image windows in Corel PaintShop Pro dark title bars and frames.

![Before and after: light blue-gray image window frames versus dark ones](https://raw.githubusercontent.com/MrSmith2017/windhawk-mod-assets/main/psp-dark-image-windows.png)

## Why

PaintShop Pro has a dark theme, but the image windows inside the workspace keep a light blue-gray frame that looks like Windows XP or 7. They are classic MDI child windows, and Windows draws their frames itself, with no dark variant.

This mod paints those frames in dark colors instead:

- title bar, border, icon and title text
- minimize, maximize and close buttons with hover and pressed states
- minimized image windows

Maximized image windows are left to Windows. Everything is drawn by the mod, so no theme files or system settings are touched, and only PaintShop Pro is affected.

## Optional flash fix

When you switch between images, PaintShop Pro rebuilds the drop-down lists in the tool options bar. For a few frames their selection fields flash white, because the Windows combo box falls back to its default brush. The flash fix paints that field in dark gray instead. It can be switched off in the settings.

## Install

1. Install [Windhawk](https://windhawk.net).
2. Open Windhawk and click **Create a new mod** (bottom right).
3. Replace the whole content of the editor with the contents of [`psp-dark-mdi-frames.wh.cpp`](psp-dark-mdi-frames.wh.cpp) from this repository.
4. Click **Compile Mod**. The mod loads into PaintShop Pro right away; no restart is needed.

Once the mod is available in the Windhawk catalog, you can install it from there with one click.

## Settings

All colors are hex codes, for example `282828` or `#282828`. A value that cannot be read falls back to its default. Changes apply right away.

| Setting | Default |
| --- | --- |
| Title bar, active / inactive | `282828` / `202020` |
| Title text, active / inactive | `ECECEC` / `828282` |
| Outer border line | `3A3A3A` |
| Thin line around the image area | `101010` |
| Button symbols, active / inactive | `E4E4E4` / `787878` |
| Button hover / pressed | `464646` / `5A5A5A` |
| Close button hover / pressed | `C42B1C` / `961E14` |
| Distance between the caption buttons | 29 px (at 100% scaling) |
| Size of the button symbols | 10 px (at 100% scaling) |
| Fix white flash in the tool options bar | on |
| Color used instead of white | `3C3C3C` |

## Compatibility

Tested with PaintShop Pro 2022 on Windows 11 (build 26100). Other versions may work but have not been tested. If something looks wrong, disable the mod in Windhawk: the original frames come back immediately.

## License

[MIT](LICENSE)
