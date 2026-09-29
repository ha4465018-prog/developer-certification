# How to Pass Technical Screening Interviews for GitHub Foundations

> **A complete step-by-step masterclass on passing GitHub Foundations (GH-900) technical screening interviews, Git branching strategies, GitHub Actions CI/CD, and Dependabot security.**

| Attribute | Details |
|---|---|
| **Category** | Exam & Interview Guide |
| **Reading Time** | 5 min read |
| **Published** | August 2026 |
| **Author** | [Careers.codes Editorial Team](https://www.linkedin.com/in/hasnain-ali-41aa042b9) |
| **Interactive Live Guide** | [Read on careers.codes](https://www.careers.codes/guides/how-to-pass-technical-screening-interviews-github-foundations) |

## Overview

Master GitHub Flow vs Git Flow branching strategies, GitHub Actions CI/CD workflows, pull request reviews, CODEOWNERS, Dependabot security, and repository administration for GH-900 interviews.

## Table of Contents

* [1. GH-900 Exam & Version Control Screening Scope](#1-gh-900-exam-version-control-screening-scope)
* [2. Git Branching Strategies: GitHub Flow vs Git Flow](#2-git-branching-strategies-github-flow-vs-git-flow)
* [3. GitHub Actions CI/CD Workflow Engineering](#3-github-actions-ci-cd-workflow-engineering)
* [4. Code Review, CODEOWNERS, & Branch Protection](#4-code-review-codeowners-branch-protection)
* [5. GitHub Security: Dependabot & Secret Scanning](#5-github-security-dependabot-secret-scanning)

---

## 1. GH-900 Exam & Version Control Screening Scope

The GitHub Foundations (GH-900) certification validates core competence in Git repository management, team collaboration, continuous integration, and security controls.

1. **Introduction to GitHub (20% Weighting):** GitHub products (Free, Team, Enterprise), Markdown documentation, GitHub Pages, User profile customization.
2. **Working with GitHub Repositories (20% Weighting):** Repository creation, Git CLI synchronization, forks, clones, release tags, repository templates.
3. **Collaboration Features (20% Weighting):** Issues, Projects (Kanban boards), Discussions, Pull Requests, Code reviews, Mentions.
4. **Modern Development Features (20% Weighting):** GitHub Actions workflows, Runners, GitHub Codespaces, Copilot integration.
5. **Privacy, Security, & Administration (20% Weighting):** Branch protection rules, Dependabot, Secret scanning, CodeQL static analysis, Organization permissions.

## 2. Git Branching Strategies: GitHub Flow vs Git Flow

**Interview Scenario:** *"Compare GitHub Flow against traditional Git Flow for agile cloud-native software teams."*

* **GitHub Flow (Lightweight & Agile):** Single persistent branch (`main`). Developers create short-lived feature branches, open Pull Requests for peer review, run automated CI tests, and deploy directly to production upon PR merge. Ideal for continuous delivery.
* **Git Flow (Structured Releases):** Multiple long-lived branches (`main`, `develop`, `release/*`, `hotfix/*`). Ideal for legacy desktop software or scheduled quarterly release cycles.

## 3. GitHub Actions CI/CD Workflow Engineering

**Interview Scenario:** *"How do you construct a YAML workflow in `.github/workflows/ci.yml` that builds, tests, and deploys a web app on pull request merges?"*

* **Triggers & Events:**
`on: push: branches: [ main ] pull_request: branches: [ main ]`
* **Jobs & Runners:** Define `jobs` executing on `runs-on: ubuntu-latest`.
* **Steps & Action Composition:**
  - `uses: actions/checkout@v4` (Fetches source repository).
  - `uses: actions/setup-node@v4` (Configures Node.js runtime).
  - `run: npm ci && npm test` (Runs deterministic test suite).
  - Use `secrets.DEPLOY_KEY` stored in GitHub Repository Secrets for secure deployment authentication.

## 4. Code Review, CODEOWNERS, & Branch Protection

**Interview Scenario:** *"How do you enforce automated governance and mandatory code reviews on the `main` branch?"*

* **Branch Protection Rules:**
  - Require a pull request before merging (enforce at least 1–2 approving reviews).
  - Require status checks to pass before merging (e.g., CI build and test suite must pass).
  - Require linear commit history (prevent merge commits).
* **`CODEOWNERS` File:** Create a `.github/CODEOWNERS` file defining mandatory reviewers by path pattern (e.g. `/src/security/ @security-team`). GitHub automatically requests review from designated owners when matching files are modified.

## 5. GitHub Security: Dependabot & Secret Scanning

**Interview Scenario:** *"How does GitHub help prevent supply chain attacks and credential leaks?"*

* **Dependabot Alerts & Security Updates:** Scans `package.json` / `requirements.txt` against the GitHub Advisory Database. Automatically opens Pull Requests updating vulnerable dependencies to patched versions.
* **Secret Scanning:** Scans commits and pull requests for exposed API tokens, AWS keys, and private SSH keys. Automatically alerts security administrators and revokes leaked tokens with partner cloud providers.
* **CodeQL (Advanced Security):** Performs semantic static application security testing (SAST) identifying SQL injection and XSS vulnerabilities during CI workflow runs.

---

### 🔗 Explore More Developer Resources

* **Live Platform:** [careers.codes](https://www.careers.codes)
* **All Guides:** [careers.codes/guides](https://www.careers.codes/guides)
* **Curator:** [Hasnain Ali on LinkedIn](https://www.linkedin.com/in/hasnain-ali-41aa042b9) & [X (Twitter)](https://x.com/HasnainAlijutt6)
