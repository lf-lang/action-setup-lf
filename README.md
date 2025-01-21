# lf-toolchain
A Github Action for installing the Lingua Franca toolchain

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
      - uses: erlingrj/lf-toolchain@stable
      - run: lingo build
```

For latest nightly release use
```yaml
      - uses: erlingrj/lf-toolchain@nightly
```