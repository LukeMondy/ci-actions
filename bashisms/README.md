<!--
  Copyright 2020, Data61, CSIRO (ABN 41 687 119 230)
  SPDX-License-Identifier: CC-BY-SA-4.0
-->

# Shell script check action

This action runs the check for [portable shell code][1] from
<https://github.com/seL4/sel4_tools> on pull requests.

[1]: https://github.com/seL4/seL4_tools/tree/master/misc/is-valid-shell-script

## Content

The main action happens in [`steps.sh`](steps.sh), the JavaScript entry point
just calls this script.

## Arguments

None

## Example

Put this into a `.github/workflows/` yaml file, e.g. `style.yml`:

```yaml
name: Style

on: [pull_request]

jobs:
  style:
    name: Shell
    runs-on: ubuntu-latest
    steps:
    - uses: seL4/ci-actions/bashisms@master
```
