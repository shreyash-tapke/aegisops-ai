<!-- CI/CD Status Badges -->
[![Tests](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/tests.yml/badge.svg)](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/tests.yml)
[![Coverage](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/coverage.yml/badge.svg)](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/coverage.yml)
[![Security](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/security.yml/badge.svg)](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/security.yml)
[![SBOM](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/sbom.yml/badge.svg)](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/sbom.yml)
[![Deployment](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/deploy.yml/badge.svg)](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/deploy.yml)
[![Release](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/release.yml/badge.svg)](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/release.yml)
[![Backup](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/backup.yml/badge.svg)](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/backup.yml)
[![Rollback](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/rollback.yml/badge.svg)](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/rollback.yml)
[![Observability](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/observability.yml/badge.svg)](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/observability.yml)
[![Cost](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/cost.yml/badge.svg)](https://github.com/shreyash-tapke/aegisops-ai/actions/workflows/cost.yml)

---

## ‚öôÔ∏è CI/CD Workflows

AegisOps AI uses GitHub Actions to enforce quality, security, and reliability across five phases of DevSecOps.  

### Ì¥π Phase 1: Testing & Quality
- **tests.yml** ‚Üí Runs unit tests on every push/PR.
- **coverage.yml** ‚Üí Generates coverage reports and uploads HTML artifacts.
- **integration-tests.yml** ‚Üí Validates integration scenarios.
- **windows-tests.yml** ‚Üí Ensures cross‚Äëplatform compatibility on Windows runners.

### Ì¥π Phase 2: Security & Compliance
- **security.yml** ‚Üí Runs Bandit to detect insecure code patterns.
- **sbom.yml** ‚Üí Generates a CycloneDX SBOM (`sbom.xml`) and uploads as artifact.

### Ì¥π Phase 3: Deployment & Release
- **deploy.yml** ‚Üí Builds Python package (wheel + source) and uploads artifacts.
- **release.yml** ‚Üí Publishes to PyPI (if secrets are set) and creates GitHub Release.

### Ì¥π Phase 4: Resilience & Backup
- **backup.yml** ‚Üí Archives project daily (or manually) and uploads backup artifacts.
- **rollback.yml** ‚Üí Restores latest backup artifact if needed.

### Ì¥π Phase 5: Observability & Cost
- **observability.yml** ‚Üí Collects CPU, memory, and disk usage logs during CI runs.
- **cost.yml** ‚Üí Tracks job duration and resource usage, uploads cost report artifact.

---

### Ìª†Ô∏è How to Use
- All workflows live in `.github/workflows/`.
- They run automatically on **push** and **pull requests**, unless marked `workflow_dispatch` (manual trigger).
- Artifacts (coverage, SBOM, backups, metrics) can be downloaded from the **Actions run page**.


---

## Ì∫Ä Quick Start

Follow these steps to set up AegisOps AI locally:

### 1. Clone the Repository
```bash
git clone https://github.com/shreyash-tapke/aegisops-ai.git
cd aegisops-ai
eof

---

## Ì¥ù Contributing Guide

We welcome contributions to **AegisOps AI**! Please follow these guidelines:

### 1. Branching Strategy
- Use feature branches: `feature/<name>`  
- Use bugfix branches: `bugfix/<issue>`  
- Never commit directly to `master`.

### 2. Commit Style
- Use clear, conventional commit messages:
  - `feat: add new module`
  - `fix: resolve import error`
  - `test: expand coverage for DB handler`
- Keep commits small and focused.

### 3. Pull Requests
- Ensure all tests pass locally (`pytest`).
- Verify coverage (`pytest --cov=. --cov-report=html`).
- Run security checks (`bandit -r .`).
- Generate SBOM (`cyclonedx-py -o sbom.xml`).
- Link related issues in the PR description.

### 4. Code Style
- Run `flake8` for linting.
- Format with `black` before committing.
- Keep functions modular and transparent.

### 5. Review Process
- At least one reviewer approval required.
- CI/CD workflows must be green before merge.
- Backups are automatically created; rollback is available if needed.

---

‚úÖ Following these rules ensures smooth collaboration and keeps AegisOps AI privacy‚Äësafe, modular, and reliable.
