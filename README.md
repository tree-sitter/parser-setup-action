# Tree-sitter parser setup

## Options

```yaml
fetch-depth:
  description: Repository fetch depth
  default: 2
submodules:
  description: Initialize submodules
  default: false
tree-sitter-ref:
  description: A tree-sitter commit, tag, or branch
  default: latest
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
      - uses: tree-sitter/parser-setup-action@v2
        with:
          submodules: true
      - uses: tree-sitter/parser-test-action@v2
```
