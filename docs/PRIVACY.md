# Privacy

- **No network.** Focus Profiles contains no networking code, and its only entitlement is Automation (`com.apple.security.automation.apple-events`). It is **not** sandboxed. Verify:

```
codesign -d --entitlements - "/Applications/Focus Profiles.app"
```

- **What it touches.** Window positions and sizes of the apps your profiles name (Accessibility); new terminal windows and browser tabs (Automation: Terminal, iTerm2, Safari, Google Chrome); `scutil --nc` for a VPN; `kubectl config use-context` for the kube context. Nothing is sent anywhere.
- **What it does not do.** It does not read window contents, record the screen, watch keystrokes, or read your browser tabs or terminal output.
- **Profiles** are plain JSON files in `~/Library/Application Support/Focus Profiles/Profiles/`. No account, no cloud.
- **Commands you write are run as written.** A terminal command in a profile is typed into a new terminal window exactly as you wrote it; only keep commands you trust.
- **Licence.** A key is verified on your Mac against a built-in public key. The app cannot create keys and sends nothing.
