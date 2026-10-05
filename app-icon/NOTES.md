# macOS app icon receipts

Images for the pull request that adds the macOS icon variants. They are renders of the bundle that
branch produces, captured on one machine:

- `app-icon-before-after.png`: the installed 2.0.14 app (before) and the packaged branch (after),
  rendered with `NSWorkspace.icon(forFile:)` under the Light and Dark system icon styles.
- `app-icon-styles.png`: the packaged branch under the Light, Dark, Clear and Tinted styles.
- `app-icon-artwork.png`: the two renditions `build/AppIcon.icon/Assets/` adds.

Environment: Apple silicon, macOS 27.2, packaged with `pnpm build:mac:arm64` and `--dir`. Each render
ran with the system icon style in `defaults read -g AppleIconAppearanceTheme` set accordingly, and
the style was restored to `RegularDark` afterwards.
