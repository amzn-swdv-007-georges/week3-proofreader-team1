# Game 1: The Automated Proofreader

## Brief

In this game, you will build a simple GitHub Actions workflow that checks Markdown files for spelling mistakes.

One student acts as the **Press Operator** and creates the automation. The other acts as the **Field Correspondent** and submits a draft containing spelling mistakes.

Your goal is to experience how GitHub Actions prevent poor-quality work from being merged into the `main` branch.

> Work concurrently. Do not wait for your partner.

---

## Instructions

### Press Operator

1. On the `main` branch, create:

```text
.github/workflows/spellcheck.yml
```

2. Copy the following workflow into the file:

```yaml
name: Spellcheck

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  spellcheck:
    name: Spellcheck Markdown Files
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v4

      - name: Run Spellcheck
        uses: streetsidesoftware/cspell-action@v6
        with:
          files: '**/*.md'
          incremental_files_only: false
          config: '{"words": ["markdown", "github", "workflow"]}'
```

3. Commit the workflow directly to `main`.

---

### Field Correspondent

1. Create a branch named:

```text
first-draft
```

2. On `first-draft`, create:

```text
draft.md
```

3. Copy one of the starter paragraphs provided by your instructor.
4. Introduce 6–8 spelling mistakes.
5. Commit the file to `first-draft`.

---

### Both Students

1. Open a Pull Request from `first-draft` into `main`.
2. Wait for the spellcheck workflow to run.
3. Review the workflow result and open the logs.
4. Identify the reported spelling mistakes.
5. Correct the mistakes and commit the changes.
6. Wait for the workflow to run again.
7. Merge the Pull Request only after all checks pass.

---

## Success Criteria

* The spellcheck workflow executes successfully.
* The Pull Request is blocked when spelling errors exist.
* The spelling errors are corrected.
* The workflow passes with a green checkmark.
* The Pull Request is merged into `main`.
