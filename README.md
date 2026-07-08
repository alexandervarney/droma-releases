# Droma

A native macOS music player for your own [Navidrome](https://www.navidrome.org)
or Subsonic‑compatible server. Album‑focused, fast, and designed to feel at home
on the Mac.

Droma streams from **your** server — your password is kept in the macOS Keychain
and never leaves your Mac.

## Download

### [⬇︎ Download the latest release](./releases)

Grab the newest `Droma-<version>.dmg` from the [releases](./releases) folder.
After you install it once, Droma keeps itself up to date automatically — it
checks for new versions and can install them for you.

**Requirements**

- macOS 15 (Sequoia) or later — Apple Silicon or Intel
- A Navidrome or Subsonic‑compatible server to connect to

## Install

1. Open the downloaded `Droma-<version>.dmg` and drag **Droma** into your
   **Applications** folder.
2. Launch Droma. Because it's distributed outside the App Store, macOS will say
   it "could not be verified." This is expected — close the dialog.
3. Open **System Settings → Privacy & Security**, scroll down, and click
   **Open Anyway** next to the message about Droma. You only need to do this
   once.

Prefer the terminal? This does the same as steps 2–3:

```sh
xattr -d com.apple.quarantine /Applications/Droma.app
```

### Verify your download (optional)

If you'd like to confirm your download is intact, compare its checksum against
the one published for that version:

```sh
shasum -a 256 ~/Downloads/Droma-<version>.dmg
```

## Privacy

Droma connects only to the server you point it at. Your credentials are stored
in the macOS Keychain and are never sent anywhere else.

---

<sub>Official download and update channel for Droma. Free to use; all rights
reserved.</sub>
