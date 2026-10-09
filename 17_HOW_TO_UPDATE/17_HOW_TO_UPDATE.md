# How to Update — SEMGREP_PRIOR_DOCS

**Project:** `SEMGREP_PRIOR_DOCS`
**Category:** SOFTWARE_DEVELOPMENT
**Domain:** software development tools
**Date:** 2026-10-08

---

## Update Procedure

### Checking for Updates
```bash
SEMGREP_PRIOR_DOCS --version
SEMGREP_PRIOR_DOCS check-update
```

### Applying Updates
```bash
pip install --upgrade SEMGREP_PRIOR_DOCS
```

### Rolling Back
```bash
pip install SEMGREP_PRIOR_DOCS==<previous-version>
```

### Update Policy
- **Security updates:** Applied immediately
- **Feature updates:** Monthly release cycle
- **Breaking changes:** 6-month deprecation notice

## Verification

16/16 PASS. Evidence: `ISOLATED_LAB_RESULTS/03_Result_Register.md`.
