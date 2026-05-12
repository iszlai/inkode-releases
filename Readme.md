# inkode

**Code quality scanning for the post-AI era.**

The `ik` CLI runs 17 checks against your codebase — secrets, vulnerable dependencies (Go, JavaScript, Python, Rust, Java), test coverage, complexity, duplication (textual *and* semantic, via an embedded LLM), coupling, and more — and gives you a 0–100 health score in under 60 seconds.

Languages: **Go, Python, JavaScript, TypeScript, Java, Rust**.

→ **[inkode.co](https://inkode.co)** · [How It Works](https://inkode.co/how-it-works/) · [Services](https://inkode.co/services/) · [CI Integration](https://inkode.co/ci/)

---

## Install

```bash
curl -fsSL https://inkode.co/install.sh | sh
```

Detects your OS and architecture, downloads the correct binary, and installs to `/usr/local/bin/ik`.

**Supported platforms:** macOS (arm64, amd64) · Linux (arm64, amd64)

**Manual download:** grab the archive for your platform from the [latest release](https://github.com/iszlai/inkode-releases/releases/latest), extract, and move `ik` to somewhere on your `$PATH`.

---

## Quick start

```bash
cd your-project
ik init        # detects languages, writes .ik.yaml
ik run         # runs all checks, prints score
```

Output:

```
inkode · your-project
Running 17 checks...

✓ Line Count             no issues       12ms
⚠ Secret Scanning        2 findings     1.1s
⚠ Test Presence          5 findings      8ms
✓ Dep Audit              no issues     890ms
✓ Semantic Duplication   no issues     3.4s
…

Score   72 / 100   grade C

Report  .ik/brief.html
Share   https://api.inkode.co/r/Xa9kLm2pQr7n
```

---

## What it checks

| Check | What it finds |
|-------|---------------|
| Secret Scanning | Hardcoded API keys, tokens, passwords (via gitleaks) |
| Dependency Audit | Known CVEs across Go, JS, Python, Rust, and Java (Maven / Gradle, via osv-scanner) |
| Test Presence | Directories with code but no tests; framework detection (JUnit, pytest, Jest, Vitest, …) |
| Complexity | Functions with high cyclomatic complexity (gocyclo, radon, ESLint, PMD) |
| Line Count | Oversized files |
| Hotspots | Files that change most frequently |
| Coupling | Files that always change together |
| Duplication | Copy-pasted code blocks |
| Semantic Duplication | Functions that do the same thing written differently — embedded LLM (Qwen2.5-Coder-0.5B), runs locally |
| Error Handling | Unchecked Go errors, bare Python excepts, empty JS/TS catches, empty / overly-broad Java catches |
| Dead Code | Unused functions, exports, variables (deadcode, vulture, knip, PMD) |
| TODO Density | High concentrations of deferred work |
| Magic Numbers | Hardcoded literals instead of named constants |
| Import Graph | Circular imports, god packages |
| Infrastructure | Dockerfile, K8s, Terraform misconfigurations |
| Scripts | Shell script vulnerabilities via ShellCheck |
| AI Stack | Which AI tools shaped the codebase (Claude Code, Copilot, Cursor, OpenAI / Anthropic SDKs, LangChain, …) |

Full details at **[inkode.co/how-it-works/](https://inkode.co/how-it-works/)**.

---

## Run on every PR (GitHub Action)

Drop a 10-line workflow into your repo and get inline annotations, a sticky PR comment, and a pass/fail check on every push. 10 free runs over 30 days — no credit card.

→ **[Wire it up at inkode.co/ci/](https://inkode.co/ci/)** · [Action source: iszlai/ik-action](https://github.com/iszlai/ik-action)

---

## Expert review

The CLI shows you where the problems are. Our engineers tell you how to fix them — prioritized by impact, delivered as a structured remediation roadmap.

**[Book a review →](https://inkode.co/services/)**

---

## Links

- **Website:** [inkode.co](https://inkode.co)
- **Case Studies:** [inkode.co/case-studies/](https://inkode.co/case-studies/)
- **Blog:** [inkode.co/blog/](https://inkode.co/blog/)
- **Issues:** [github.com/iszlai/inkode-releases/issues](https://github.com/iszlai/inkode-releases/issues)
