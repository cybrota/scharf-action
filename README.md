# scharf-action
A GitHub action to detect mutable third-party references used in GitHub repository.

This uses Scharf tool to identify actions with mutable tags.

## Usage

```yaml
jobs:
  run-unit-tests:
    runs-on: ubuntu-22.04

    steps:
      - name: Checkout repository
        uses: actions/checkout@11bd71901bbe5b1630ceea73d27597364c9af683

      - name: Audit GitHub actions
        uses: cybrota/scharf-action@71662a3ec833b0c915a67f21e500e81786b95901 #v1
        with:
          raise-error: true
```

## Inputs

* raise-error (Raises Exit 1 error if any violating actions found. Default is false)

## Links
* https://github.com/cybrota/scharf
