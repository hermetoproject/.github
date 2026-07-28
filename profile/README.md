# Hermeto Project

Hermeto is a CLI tool that downloads your project's dependencies ahead of time
so that container builds can run without network access. It also generates
accurate SBOMs (Software Bill of Materials) covering every pre-fetched
dependency, notably including every transitive dependency as well.

## Why Hermeto exists

Without network isolation, builds can silently pull tampered packages, produce
unreproducible artifacts, or hide dependencies from your audit trail. Hermeto
solves this by fetching all declared dependencies ahead of time, verifying
their integrity, and generating a complete software bill of materials.

## Supported languages

  - **Go**: gomod
  - **Java**: maven (experimental)
  - **JavaScript**: npm, pnpm, yarn (classic and berry)
  - **Python**: pip
  - **Ruby**: bundler
  - **Rust**: cargo
  - **Other**: rpm, generic

## Get Involved

For contributing, check out [CONTRIBUTING.md](../CONTRIBUTING.md).

For AI-assisted contributions, make sure to comply with the [AI_CONTRIBUTION_POLICY.md](../AI_CONTRIBUTION_POLICY.md).
