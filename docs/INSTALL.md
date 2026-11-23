# Install Focus Profiles

Requires macOS 27 or later on Apple silicon. Focus Profiles is a menu-bar app with no Dock icon.

## 1. Download and verify

Download [FocusProfiles-0.2.0.dmg](https://github.com/zyvorai/focus/releases/download/v0.2.0/FocusProfiles-0.2.0.dmg) and its `.sha256` file from the [release page](https://github.com/zyvorai/focus/releases/tag/v0.2.0). The DMG is Developer ID signed and notarized by Apple.

```
shasum -a 256 -c FocusProfiles-0.2.0.dmg.sha256
xcrun stapler validate FocusProfiles-0.2.0.dmg
```

SHA-256 of this release: `bfabd31ff93479f6d71ed8000e0466dc6ae0bed42471c94b9b91a316d098a850`.

## 2. Install

Open the DMG, drag **Focus Profiles** to Applications and open it. A Welcome window explains each permission before anything is requested.

## 3. Trial key

You do not need a key. For a 30-day trial key write to sales@zyvor.dev. Enter a trial key under **Licence…** in the menu. See [LICENSING.md](LICENSING.md).

## Permissions

- **Accessibility** is requested when you first switch a profile that places windows.
- **Automation** is asked by macOS per app (Terminal, iTerm2, Safari, Google Chrome) the first time a profile uses it.
- VPN and kube context need no permission (`scutil` and `kubectl` must be present).

Open **System Settings > Privacy & Security** to change any of them later.

## Uninstall

Quit Focus Profiles and delete it from Applications. Your profiles are plain files in `~/Library/Application Support/Focus Profiles/Profiles/`; delete that folder to remove them.
