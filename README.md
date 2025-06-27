# Reusable Workflows

This repository contains reusable GitHub Actions workflows for consistent automation across multiple projects.

## 🔁 Reusable Release Workflow

### Usage

```yaml
jobs:
  release:
    uses: https://github.com/Vronst/release_workflow
    with:
      python-version: '3.13'
    secrets:
      TOKEN: ${{ secrets.PRO_TOKEN }}
```
