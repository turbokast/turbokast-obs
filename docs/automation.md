# Project automation

Nothing here needs a paid service. Third-party reviewers are advisory: they can comment, but they are never a required check. Fork pull requests get no secrets and a read-only token.

| Automation | What it does | Where |
|---|---|---|
| CI (`CI OK`) | rustfmt, clippy, tests and build on Linux and Windows, cargo-deny, REUSE, gitleaks, actionlint | `workflows/ci.yml`, `deny.toml`, `REUSE.toml` |
| DCO (`DCO sign-off`) | Fails a pull request with a commit lacking `Signed-off-by` | `workflows/dco.yml` |
| Dependency review | Blocks new dependencies with moderate or worse advisories, or licences outside the allow-list | `workflows/dependency-review.yml` |
| CodeQL | Security analysis of Rust and the workflows | `workflows/codeql.yml` |
| OSV-Scanner | Scans `Cargo.lock` against the OSV database | `workflows/osv-scanner.yml` |
| OpenSSF Scorecard | Publishes a supply-chain score | `workflows/scorecard.yml` |
| zizmor | Security audit of the workflows | `workflows/zizmor.yml` |
| Dependabot | Weekly grouped updates for actions and crates, after a 7-day cooldown, plus security updates | `dependabot.yml` |
| PR title, labeler, release drafter, stale, lock, welcome | Housekeeping | `workflows/` |
| CodeRabbit, Sourcery | Advisory AI review | `.coderabbit.yaml`, Sourcery dashboard |
| Socket, GitGuardian, Snyk, Codacy, SonarQube Cloud | Advisory supply-chain, secret, vulnerability and code-quality checks | GitHub Apps, configured in each service's dashboard |

GitHub secret scanning with push protection and private vulnerability reporting are repository settings.

Plugin checks (clang-format, clang-tidy, sanitizers) and release jobs join when that code arrives.
