# Compile PHP - GitHub Actions

This GitHub action downloads the latest Curl release (curl),
configures it to enable all features, compiles it, and installs it.

## Usage

```yaml
name: Tests
permissions: read-all
on:
  pull_request:
  push:

jobs:
  run:
    runs-on: ubuntu-latest
    name: Compile and install PHP - Test
    steps:
      - name: Setup PHP
        uses: PHPWatch/setup-curl@main

      - name: Display versions and env
        run: |
          curl --version

```
