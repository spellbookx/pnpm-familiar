# pnpm familiar⚡

> A GitHub Action that conjures a fully cached, version-aligned pnpm environment — your reliable familiar for fast, reproducible CI pipelines.

![Tests](https://github.com/spellbookx/pnpm-familiar/actions/workflows/release.yml/badge.svg)

## Features

- 🌀 Fully reproducible with `.nvmrc`-based Node.js resolution
- ⚡ Intelligent caching via `pnpm`
- 🧩 Drop-in composite action — no JS or Docker required
- 🔮 Customizable via inputs like `skip-build`

## Usage

```yaml
# .github/workflows/test.yml
name: CI

on:
  push:
  pull_request:

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - uses: spellbookx/pnpm-familiar@v1

      - name: Run Tests
        run: pnpm test
```

### Inputs

| Name         | Description                  | Default   |
| ------------ | ---------------------------- | --------- |
| `skip-build` | If true, skips `pnpm build`. | `"false"` |

## Author

Made by [@ctrlmaniac](https://github.com/ctrlmaniac) at [@spellbookx](https://github.com/spellbookx)
