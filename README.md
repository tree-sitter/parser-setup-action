# Tree-sitter parser setup

## Options

```yaml
fetch-depth:
  description: Repository fetch depth
  default: 2
submodules:
  description: Initialize submodules
  default: false
node-version:
  description: NodeJS version
  default: latest
rust-toolchain:
  description: Rust toolchain
  default: stable
```

## Example configuration

```yaml
name: CI

on:
  push:
    branches: [master]
  pull_request:

jobs:
  test:
    name: Run tests
    runs-on: ubuntu-latest
    steps:
      - uses: tree-sitter/parser-setup-action@v1.2
        with:
          node-version: 20
      - uses: tree-sitter/parser-test-action@v1.2
```
