# renovate-config-validator-workflow [![test](https://github.com/int128/renovate-config-validator-workflow/actions/workflows/test.yaml/badge.svg)](https://github.com/int128/renovate-config-validator-workflow/actions/workflows/test.yaml)

This is a reusable workflow to run [renovate-config-validator](https://docs.renovatebot.com/config-validation/) in your repository.

## Getting Started

```yaml
name: renovate-config

on:
  pull_request:
    paths:
      - .github/workflows/renovate-config.yaml
      - .github/renovate.*
  push:
    branches:
      - main
    paths:
      - .github/workflows/renovate-config.yaml
      - .github/renovate.*

jobs:
  validate:
    uses: int128/renovate-config-validator-workflow/.github/workflows/validate.yaml@main
```

## How it works

This workflow runs renovate-config-validator in the container image of Renovate Bot using [renovatebot/github-action](https://github.com/renovatebot/github-action).
