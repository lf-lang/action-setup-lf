# lf-toolchain
A Github Action for installing the Lingua Franca toolchain

<br>
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
      - uses: erlingrj/lf-toolchain
        with:
          toolchain: stable
          components: lingo
      - run: lingo build
```
<br>

## Inputs

<table>
<tr>
  <th>Name</th>
  <th>Description</th>
</tr>
<tr>
  <td><code>toolchain</code></td>
  <td>
    LF toolchain specifier e.g. <code>stable</code> or <code>nightly</code>
  </td>
</tr>
<tr>
</tr>
<tr>
  <td><code>components</code></td>
  <td>Comma-separated string of additional components to install e.g. <code>lingo</code></td>
</tr>
</table>

<br>
