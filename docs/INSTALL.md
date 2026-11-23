# Install Focus Profiles

Requires macOS 27 or later on Apple silicon. Focus Profiles is a menu-bar app with no Dock icon.

## 1. Get the download

No public download is posted yet. Write to [sales@zyvor.dev](mailto:sales@zyvor.dev?subject=Focus%20Profiles%20trial%20key) for a 30-day trial key; we send the notarized, Developer ID signed DMG with it. Verify it:

```
shasum -a 256 -c Focus-Profiles-<version>.dmg.sha256
xcrun stapler validate Focus-Profiles-<version>.dmg
```

## 2. Install

Open the DMG, drag **Focus Profiles** to Applications and open it. A Welcome window explains each permission before anything is requested.

## 3. Trial key

You do not need a key. Enter a trial key under **Licence…** in the menu. See [LICENSING.md](LICENSING.md).

## Permissions

- **Accessibility** is requested when you first switch a profile that places windows.
- **Automation** is asked by macOS per app (Terminal, iTerm2, Safari, Google Chrome) the first time a profile uses it.
- VPN and kube context need no permission (`scutil` and `kubectl` must be present).

Open **System Settings > Privacy & Security** to change any of them later.

## Uninstall

Quit Focus Profiles and delete it from Applications. Your profiles are plain files in `~/Library/Application Support/Focus Profiles/Profiles/`; delete that folder to remove them.
