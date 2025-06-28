# Reusable Workflows

This repository contains reusable GitHub Actions workflows for consistent automation across multiple projects.

## 🔁 Reusable Release Workflow

### Usage

- create release-notes.txt (can be empty) -> will be used to generete release notes
- create release-title.txt (can be empty) -> will be used for release title

```yaml
# Exapmle job
name: test

on:
  push:
    branches:
      - main

# needed permissions
permissions:
  contents: write
  packages: write

# This is most important part
# This uses release workflow
jobs:
  release:
    uses: Vronst/release_workflow/.github/workflows/release.yml@1.0.0
    with:
      python-version: '3.13'
    secrets:
      TOKEN: ${{ secrets.PRO_TOKEN }}
```

- PRO_TOKEN = token with permission to create releases
