# Ì¥ç GitHub Actions Tab Guide

This guide explains how to use the **Actions tab** in GitHub to monitor workflows for AegisOps AI.

---

## Ì≥ä Viewing Workflow Runs
- Navigate to the **Actions tab** in the repository.
- Each commit or pull request triggers workflows (Tests, Coverage, Security, Release, Backup, Observability).
- Click on a workflow run to see detailed logs.

---

## Ì≥Ç Downloading Artifacts
- Inside a workflow run, scroll to the **Artifacts** section.
- Available artifacts include:
  - Coverage reports (`htmlcov`)
  - SBOM (`sbom.xml`)
  - Backup archives (`project-backup`)
  - Metrics logs (`system-metrics`)
  - Cost reports (`cost-report`)
- Click the artifact name to download.

---

## ‚ö†Ô∏è Debugging Failing Runs
- Red ‚ùå indicates a failing workflow.
- Expand the failing job to see error logs.
- Common issues:
  - **Tests failing** ‚Üí Run `pytest` locally.
  - **Coverage threshold not met** ‚Üí Check `pytest --cov`.
  - **Security scan issues** ‚Üí Run `bandit -r .`.
  - **SBOM errors** ‚Üí Ensure `cyclonedx-py` is installed.

---

## ‚úÖ Best Practices
- Always check workflow status before merging a PR.
- Use artifacts to reproduce issues locally.
- Communicate failures in PR comments with logs attached.

