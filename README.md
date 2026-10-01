# vendored-assets

Vendored binary assets that templates in [d77void-pkgs](https://github.com/dani-77/d77void-pkgs)
need but aren't shipped in the upstream project's own source tarball.

Each asset is published as a GitHub Release, referenced from the relevant
`distfiles=` entry in the template, pinned by sha256 checksum like any
other distfile.

## Assets

- **mullvadbrowser-noto-fonts** — the Noto/Arimo/Tinos/Cousine/STIX font set
  Mullvad Browser bundles for anti-fingerprinting (identical set everyone
  renders with, regardless of host system fonts). Comes from the Tor
  Browser Build `fonts` project (pinned Noto git hash), which isn't part of
  the mullvad-browser gecko source tree we build from. Extracted from
  Mullvad's own official `.deb` release, excluding `fonts.conf` and
  `TwemojiMozilla.ttf` (those two are already produced by our build via
  `--enable-bundled-fonts`).
