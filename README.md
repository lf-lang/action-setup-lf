# action-setup-lf
A Github Action for installing the Lingua Franca toolchain, including `lfc` and `lingo`.

## Requirements
The Github Action only supports workflows running on Linux and macOS hosts.

## Example workflow

```yaml
name: CI
on: [push, pull_request]

jobs:
  test:
    name: lingo build
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: lf-lang/action-setup-lf@v0.2
        with:
          lfc-version: stable
          lingo-version: stable
      - run: lingo build
```

For latest nightly release of lfc and v0.2.0 of lingo:
```yaml
      - uses: lf-lang/action-setup-lf@v0.2
        with:
          lfc-version: nightly
          lingo-version: 0.2.0

```

## Inputs
- `lfc-version`: Which version of LFC to install. Currently only support for `nightly` or `stable`
- `lingo-version`: Which version of lingo to install. Either `stable` or a version number.

