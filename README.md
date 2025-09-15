# ci-action-rdme

Github CI action to install and run [cargo-rdme](https://crates.io/crates/cargo-rdme)

## Inputs

_None_

## Usage

```yaml
name: CI
on:
  push:
    branches: [ master ]
  pull_request:
    branches: [ master ]
  workflow_dispatch:

jobs:
  readme:
    name: Check if README is up to date
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v5
      - id: cargo-rdme
        uses: rusticata/ci-action-rdme@master
```
