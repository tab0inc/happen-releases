# Happen Releases

This repository is the public binary distribution channel for Happen. The
source repository is private. All distributed software remains proprietary to
Tab0 Inc.

## Install

Install the latest signed and notarized macOS release (Apple silicon and Intel)
with Homebrew, then prepare this Mac once and start the server:

```bash
brew install tab0inc/tap/happen
happen setup
brew services start happen
```

Each release includes `happen_<version>_darwin_arm64.tar.gz`,
`happen_<version>_darwin_amd64.tar.gz`, and SHA-256 checksums in
`happen_<version>_checksums.txt`.

## Security

Report vulnerabilities privately by following [`SECURITY.md`](SECURITY.md).
Do not publish credentials, access tokens, or private messages.

## License

Copyright (c) 2026 Tab0 Inc. All rights reserved. Official binary releases may
be used only under the limited terms in [`LICENSE`](LICENSE). No open-source
license is granted.
