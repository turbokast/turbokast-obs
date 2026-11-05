# Contributing

Issues and pull requests are welcome. For anything large, open an issue first.

## Sign off your commits

This project uses the [Developer Certificate of Origin](DCO) and has no CLA. Sign every commit with `git commit -s`. The `Signed-off-by` line must match the commit author.

Contributions to `contracts/` are accepted under MIT, contributions to `docs/` under CC-BY-4.0, and everything else under GPL-2.0-or-later.

## Before you open a pull request

```sh
cargo fmt --all --check
cargo clippy --workspace --all-targets
cargo test --workspace
cargo deny check
```

## Pull request titles

Titles follow [Conventional Commits](https://www.conventionalcommits.org/), for example `fix(companion): retry the handshake`. Pull requests are squash-merged, so the title becomes the commit message.

## Never post private data

Do not put stream keys, tokens, recordings or real chat logs in an issue, a pull request or a fixture. Redact diagnostics first, and keep fixtures synthetic.
