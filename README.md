# Week 3 – Team 1 Repository

## Overview

This repository is the `Team 1` workspace for the Week 3 Games. The team will progressively build GitHub Actions workflows, validate content quality, investigate pipeline failures, publish a release, repair broken workflows, and implement automated security scanning.

## Repository Structure

```text
.
├── .github
│   └── workflows
│       ├── spellcheck.yml          # Game 1: Automated Proofreader
│       ├── markdownlint.yml        # Game 2: Layout Enforcer
│       ├── printingpresslint.yml   # Game 3: Printing Press Jam
│       ├── repair_job.yml          # Game 5: Press Schematics
│       └── redactor.yml            # Game 6: The Redactor
├── draft.md                        # Game 1
├── editorial_draft.md              # Game 2
├── chapters/                       # Game 3
├── RELEASE.md                      # Game 4
└── expense_reports.md              # Game 6
```

## Workflows

| Workflow                | Game   | Purpose                                                            |
| ----------------------- | ------ | ------------------------------------------------------------------ |
| `spellcheck.yml`        | Game 1 | Detect spelling mistakes before merge.                             |
| `markdownlint.yml`      | Game 2 | Enforce Markdown formatting and layout standards.                  |
| `printingpresslint.yml` | Game 3 | Validate shared anthology content during collaborative publishing. |
| `repair_job.yml`        | Game 5 | Demonstrate workflow troubleshooting and YAML repair.              |
| `redactor.yml`          | Game 6 | Detect exposed secrets and credentials before merge.               |

## Release

| Artifact                | Game   | Purpose                                                |
| ----------------------- | ------ | ------------------------------------------------------ |
| GitHub Release `v1.0.0` | Game 4 | Publish the first validated edition of the repository. |
