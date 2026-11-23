# FAQ

**What is a profile?**

A saved working context for one project: where its windows go, which terminal windows and browser tabs to open, whether to connect a VPN, and which kube context to use. Each profile can have its own hotkey.

**Can I see what a switch will do first?**

Yes. The Dry Run button in the editor and `FocusProfiles --dry-run` print every step, including what would be skipped for missing permissions. A dry run moves nothing, launches nothing and prompts for nothing.

**Which permissions does it need, and when?**

Accessibility, to move windows: asked when you first switch a profile that places windows. Automation, to open windows and tabs in Terminal, iTerm2, Safari or Chrome: asked by macOS once per app. If you refuse, only those steps are skipped and reported; the rest of the profile still runs.

**Does it send anything over the network?**

No. It contains no networking code and its only entitlement is Automation. Check with `codesign -d --entitlements - "/Applications/Focus Profiles.app"`. It is not sandboxed.

**Does it read my windows, tabs or terminal output?**

No. It moves and resizes windows, and asks apps to open new windows and tabs. It does not read their contents.

**Where are my profiles?**

Plain JSON files in `~/Library/Application Support/Focus Profiles/Profiles/`, one per profile. Edit them in the app or by hand.

**Is there a trial?**

Yes: a 30-day trial key from sales@zyvor.dev. Without a key everything still works.

**What happens without a key, or when a trial ends?**

Nothing is disabled. A status line shows where your licence stands.

**How much does it cost?**

INR 1,999 per Mac, one-time, incl. 18% GST in India and one year of updates (about US$20 excl. tax outside India). Teams of 5 or more Macs: INR 1,699 per Mac (about US$17 excl. tax), minimum 5 Macs (INR 8,495, about US$86), by invoice. Prices: INR incl. 18% GST in India; US dollars excl. tax elsewhere (VAT, GST or sales tax added where applicable). Standard orders: pay online with Razorpay (UPI, card, netbanking). Bigger orders, team and volume orders, and customers outside India: we send a US-dollar invoice and you pay through Skydo (international bank transfer, or card/ACH through a secure Skydo link). Custom pricing: contact sales@zyvor.dev. Buy: [zyvor.dev/buy](https://zyvor.dev/buy#focus-profiles).

**Which macOS versions?**

macOS 27 or later, Apple silicon.
