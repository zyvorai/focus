# Changelog

## v0.2.0 - 2026-11-23

First public release (trial). Requires macOS 27 or later, Apple silicon.

- One profile per project, one hotkey per profile. Window layout (Accessibility API), terminal windows (Terminal, iTerm2), browser tabs (Safari, Google Chrome), VPN (`scutil --nc`), kube context (`kubectl`).
- **New in 0.2.0:** open files, folders and http(s) pages (optionally in a chosen app); run Apple Shortcuts; hide the other apps; **Switch Back** restores the windows the last switch moved; Duplicate Profile; Command-1 to 9 for the first nine profiles in the menu.
- Dry run (`--dry-run` and the editor button) that touches nothing.
- **Fix:** the first use of Terminal, iTerm2, Safari or Chrome could freeze the app while macOS asked for Automation permission; it is now handled without blocking the app. A hand-written VPN entry without `connect` now loads.
- Permissions are asked only when a profile first needs them; denied steps are skipped and reported while the rest still runs.
- Plain JSON profile files. Soft licence: never disables a feature. Free 30-day trial key: sales@zyvor.dev.
