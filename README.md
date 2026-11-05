# TurboKast for OBS

[![CI](https://github.com/turbokast/turbokast-obs/actions/workflows/ci.yml/badge.svg)](https://github.com/turbokast/turbokast-obs/actions/workflows/ci.yml)
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/turbokast/turbokast-obs/badge)](https://scorecard.dev/viewer/?uri=github.com/turbokast/turbokast-obs)

An open-source OBS Studio plugin, dock and local companion for [TurboKast](https://turbokast.com) multistreaming.

**Status: nothing to install yet.** This repository holds the project skeleton and its checks. The plugin and companion are not implemented.

## Layout

| Path | Contents | Licence |
|---|---|---|
| `plugin/` | Native plugin and dock | GPL-2.0-or-later |
| `companion/` | Rust companion process | GPL-2.0-or-later |
| `simulator/` | Offline simulator of the cloud contracts | GPL-2.0-or-later |
| `packaging/` | Installers and update client | GPL-2.0-or-later |
| `tests/` | Cross-component tests | GPL-2.0-or-later |
| `contracts/` | Protocol schemas and fixtures | MIT |
| `docs/` | Documentation | CC-BY-4.0 |

## Build

```sh
cargo test --workspace
cargo run -p turbokast-companion
```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Report security issues through [SECURITY.md](SECURITY.md).

## Licence and trademarks

Licensing is per directory, as above, and the full texts are in [LICENSES/](LICENSES/). The TurboKast name and logo are not licensed under these terms.

OBS Studio is named only to describe compatibility. This project is not affiliated with or endorsed by the OBS Project.
