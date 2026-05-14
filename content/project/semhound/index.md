---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "semhound"
subtitle: "Org-scale Semgrep sweeps with optional AI triage"
summary: "A Python CLI that discovers every repository in one or more GitHub organisations or users, shallow-clones them in parallel, runs your Semgrep rules, and writes a consolidated CSV (and optional SARIF) with permalinks to each finding. Optionally send each finding to Claude, OpenAI, Gemini, or AWS Bedrock for confidence scoring and true-positive triage."
authors: [rohit]
tags: [security, appsec, sast, semgrep, threat-hunting, python, github, devsecops, ai-triage]
categories: [Security]
date: 2026-05-14T12:00:00+05:30
featured: true
draft: false
toc: true

image:
  caption: "semhound"
  focal_point: "smart"
  preview_only: false

url_code: "https://github.com/salecharohit/semhound"
url_pdf: ""
url_slides: ""
url_video: ""
slides: ""
---

## Motivation

Security teams often need the same answer across **many** repositories: “Where else does this pattern show up?” That might be a bug-bounty SQLi variant, a zero-day in a dependency, or a custom policy you encode as Semgrep rules. Running Semgrep repo-by-repo means scripting discovery, cloning, execution, and reporting yourself.

**semhound** automates that loop at GitHub org (or user) scale: you supply the rules, it handles **discovery** (`gh repo list`), **parallel shallow clones** over SSH, **scanning**, and a **single report** per target with GitHub permalinks. If you want help separating noise from signal, optional **AI triage** adds a confidence score and a true-positive verdict per finding.

The mental model is simple: tools like TruffleHog or Gitleaks are built for **secrets**; semhound is for **any Semgrep pattern** you define, swept across every repo you can access—like a hound for Semgrep findings.

## What it does

1. **Discover** — Lists repositories for each org or username you pass (inline or via `--orgs-file`).
2. **Clone** — Shallow clone (`--depth 1`) with a blob size cap aligned to Semgrep’s default so large binaries are skipped.
3. **Scan** — Runs your rules from a local `--rules-dir`, remote `--rules-url`, or both.
4. **Report** — Writes `<target>_scan.csv` and optional SARIF (`--sarif`).

semhound is aimed at **targeted, on-demand** investigations (tight rule sets, specific events), not continuous full-org scanning with huge rule packs.

## Install and docs

- **PyPI**: [https://pypi.org/project/semhound/](https://pypi.org/project/semhound/) — `pipx install semhound` is the recommended install path.
- **Source and full README**: [https://github.com/salecharohit/semhound](https://github.com/salecharohit/semhound) — prerequisites (`gh`, `git`, `semgrep`, SSH to GitHub), usage examples, AI provider configuration (`ai.config.example`), output column reference, and FAQ.

If you use private repositories, you need `gh auth login` plus an SSH key registered with GitHub for cloning.

## Licence

Open source under the **MIT** licence; see the repository for details.
