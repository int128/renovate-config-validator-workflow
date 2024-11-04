# renovate-config-validator-workflow [![test](https://github.com/int128/renovate-config-validator-workflow/actions/workflows/test.yaml/badge.svg)](https://github.com/int128/renovate-config-validator-workflow/actions/workflows/test.yaml)

This is a reusable workflow to run [`renovate-config-validator`](https://docs.renovatebot.com/config-validation/) in your repository.

## Getting Started

```yaml
name: validate

on:
  pull_request:
  push:
    branches:
      - main

jobs:
  validate:
    uses: int128/renovate-config-validator-workflow/.github/workflows/validate.yaml@main
    with:
      config: .github/renovate.* *.json
```

## How it works

This workflow runs `renovate-config-validator` using pnpm on Node.js.
