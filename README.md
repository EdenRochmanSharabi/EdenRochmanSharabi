# Hi, I'm Eden

Software engineer based in Spain.

## Open Source Contributions

### [AeroSpace](https://github.com/nikitabobko/AeroSpace) — macOS tiling window manager

- **Native tab detection** — Fixed a long-standing bug ([#68](https://github.com/nikitabobko/AeroSpace/issues/68)) where macOS native tabs were treated as separate windows, causing incorrect tiling. Uses `CGWindowListCopyWindowInfo` (public API) to detect inactive tabs without relying on private APIs.
- **Focus follows mouse** — Implemented `focus-follows-mouse` config option ([#12](https://github.com/nikitabobko/AeroSpace/issues/12)) with debounced mouse tracking and automatic window focus.
- **Sticky floating windows** — Implemented the `sticky` command ([#2](https://github.com/nikitabobko/AeroSpace/issues/2)) allowing floating windows to persist across workspace switches.
