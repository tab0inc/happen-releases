# Happen Releases

[Happen](https://happen.run) is a Mac app for handing work to Claude Code: an
AI works in each space, its workers take the work on in parallel, and only what
you need to decide comes to your phone, with a recommendation and why.

This repository is the public binary distribution channel for Happen. The
source repository is private. All distributed software remains proprietary to
Tab0 Inc.

## Install

Happen needs an Apple silicon Mac with macOS 13 or later.

- Download the disk image from [happen.run/download/mac](https://happen.run/download/mac)
  (the latest release's `Happen_<version>.dmg`), open it, and drag Happen to
  Applications.
- Or install it with Homebrew:

  ```bash
  brew install --cask tab0inc/tap/happen
  ```

Then follow [Getting started](https://happen.run/docs/getting-started). Happen
is free for 14 days, then a one-time license ([pricing](https://happen.run/#price)).

The app updates itself. `brew upgrade` leaves it alone, because the cask is
marked `auto_updates`.

## Release files

Each release includes:

- `Happen_<version>.dmg`: the signed and notarized app, for a first install.
- `Happen_<version>.zip`: the same app, which the app's updater downloads.
- `appcast.xml`: the update feed the app reads.
- `happen_<version>_checksums.txt`: SHA-256 checksums of the disk image and
  the zip.

What changed in each version: [release notes](https://happen.run/release-notes).

## Upgrading from 0.12.0 or earlier

From 0.13.0 Happen ships only as the Mac app. The Homebrew formula, the install
script, Linux, WSL, and Intel builds ended with 0.12.0. If you installed one of
those, stop and remove its server, then install the app. Your settings and data
carry over.

```bash
# Homebrew formula
brew services stop happen && brew uninstall --formula happen

# Install script
launchctl bootout gui/$(id -u)/ai.tab0.happen.binary
rm -rf ~/Library/LaunchAgents/ai.tab0.happen.binary.plist ~/.local/share/happen ~/.local/bin/happen
```

## Support and security

Questions and problems: [happen.run/support](https://happen.run/support) or
support@happen.run.

Report vulnerabilities privately by following [`SECURITY.md`](SECURITY.md).
Do not publish credentials, access tokens, or private messages.

## License

Copyright (c) 2026 Tab0 Inc. All rights reserved. Official binary releases may
be used only under the limited terms in [`LICENSE`](LICENSE). No open-source
license is granted.
