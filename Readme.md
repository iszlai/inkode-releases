# inkode releases

Binary releases for [`ik`](https://inkode.co) — the automated codebase quality analyzer built for the post-AI era.

## Install

**One line:**

```sh
curl -fsSL https://inkode.co/install.sh | sh
```

This downloads the latest `ik` binary for your OS and architecture and installs it to `/usr/local/bin/ik`.

**Or download manually** from the [releases page](https://github.com/iszlai/inkode-releases/releases) and place the binary somewhere on your `PATH`.

## Platforms

| OS      | Architecture |
|---------|-------------|
| macOS   | arm64 (Apple Silicon) |
| macOS   | amd64 (Intel) |
| Linux   | amd64 |
| Linux   | arm64 |

## Quick start

```sh
# Initialize a project (creates .ik.yaml)
ik init

# Run all checks against the current repo
ik run

# Open the full report in your browser
ik review
```

## What it checks

`ik` runs 8 automated checks concurrently and produces a scored report:

| Check | What it finds |
|-------|--------------|
| `secrets` | Hardcoded credentials and API keys |
| `dep-audit` | Known CVEs in dependencies |
| `test-presence` | Directories with no test coverage |
| `duplication` | Copy-pasted code blocks |
| `coupling` | Hidden architectural coupling via co-change patterns |
| `complexity` | Functions with high cyclomatic complexity |
| `line-count` | Oversized files |
| `hotspot` | High-churn files most likely to introduce bugs |

Results are graded A–F. Reports can be shared as a public teaser URL or reviewed in full locally.

## Source & docs

Full source, documentation, and self-hosting instructions live in the main repository:
[github.com/iszlai/inkode](https://github.com/iszlai/inkode)
