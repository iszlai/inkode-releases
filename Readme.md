# inkode

**Code quality scanning for the post-AI era.**

The `ik` CLI runs 15 checks against your codebase — secrets, vulnerable dependencies, test coverage, complexity, duplication, coupling, and more — and gives you a 0–100 health score in under 60 seconds.

→ **[inkode.co](https://inkode.co)** · [How It Works](https://inkode.co/how-it-works.html) · [Services](https://inkode.co/services.html)

---

## Install

```bash
curl -fsSL https://inkode.co/install.sh | sh
```

Detects your OS and architecture, downloads the correct binary, and installs to `/usr/local/bin/ik`.

**Supported platforms:** macOS (arm64, amd64) · Linux (arm64, amd64)

**Manual download:** grab the archive for your platform from the [latest release](https://github.com/iszlai/inkode/releases/latest), extract, and move `ik` to somewhere on your `$PATH`.

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
Running 15 checks...

✓ Line Count      no issues    12ms
⚠ Secret Scanning 2 findings   1.1s
⚠ Test Presence   5 findings   8ms
✓ Dep Audit       no issues    890ms
...

Score  72 / 100   grade C

Report  .ik/brief.html
```

---

## What it checks

| Check | What it finds |
|-------|---------------|
| Secret Scanning | Hardcoded API keys, tokens, passwords |
| Dependency Audit | Known CVEs in Go, JS, Python dependencies |
| Test Presence | Directories with code but no tests |
| Complexity | Functions with high cyclomatic complexity |
| Line Count | Oversized files |
| Hotspots | Files that change most frequently |
| Coupling | Files that always change together |
| Duplication | Copy-pasted code blocks |
| Error Handling | Unchecked errors, bare excepts, empty catches |
| Dead Code | Unused functions, exports, variables |
| TODO Density | High concentrations of deferred work |
| Magic Numbers | Hardcoded literals instead of named constants |
| Import Graph | Circular imports, god packages |
| Infrastructure | Dockerfile, K8s, Terraform misconfigurations |
| Scripts | Shell script vulnerabilities via ShellCheck |

Full details at **[inkode.co/how-it-works.html](https://inkode.co/how-it-works.html)**

---

## Expert review

The CLI shows you where the problems are. Our engineers tell you how to fix them — prioritized by impact, delivered as a structured remediation roadmap.

**[Book a review →](https://inkode.co/services.html)**

---

## Links

- **Website:** [inkode.co](https://inkode.co)
- **Case Studies:** [inkode.co/case-studies.html](https://inkode.co/case-studies.html)
- **Issues:** [github.com/iszlai/inkode/issues](https://github.com/iszlai/inkode/issues)