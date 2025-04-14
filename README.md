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
        uses: cybrota/scharf-action@c0d0eb13ca383e5a3ec947d754f61c9e61fab5ba
        with:
          raise-error: true
```

## Inputs

* raise-error (Raises Exit 1 error if any violating actions found. Default is false)

## Links
* https://github.com/cybrota/scharf
