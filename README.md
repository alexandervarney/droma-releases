# Droma Releases

Public download + auto-update channel for [Droma](https://github.com/alexandervarney/droma),
a native macOS music player for Navidrome/Subsonic servers. The application
source lives in a separate, private repository; this repository only hosts the
release artifacts so they are reachable without a login.

## Layout

- `appcast.xml` — the [Sparkle](https://sparkle-project.org) update feed. The app
  reads it from
  `https://raw.githubusercontent.com/alexandervarney/droma-releases/main/appcast.xml`.
- `releases/` — the signed `Droma-<version>.dmg` files the appcast points at.

## Publishing a release

From a checkout of the Droma source repo, run `Scripts/release.sh`. It builds the
DMG, EdDSA-signs it, and writes `dist/publish/{appcast.xml, releases/*.dmg}`.
Copy those into this repository, commit, and push. Updates are verified against
the EdDSA public key embedded in the app; the private key never leaves the
release Mac's Keychain.
