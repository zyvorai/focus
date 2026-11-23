# Changelog

## Unreleased

No public release has been posted yet. 30-day trial builds are sent on request: sales@zyvor.dev.

Focus Profiles 0.1.0 (the version in trial) does this:

- One profile per project, one hotkey per profile.
- Window layout through the Accessibility API; terminal windows (Terminal, iTerm2) and browser tabs (Safari, Google Chrome) through Automation; VPN through `scutil --nc`; kube context through `kubectl`.
- Dry run (`--dry-run` and the editor button) that touches nothing.
- Permissions are asked only when a profile first needs them; denied steps are skipped and reported while the rest still runs.
- Plain JSON profile files. Soft licence: never disables a feature.
