# ci-required-checks-test

Even if a status check is required, a PR can be merged when skipped:

```yml
jobs:
  test987:
    runs-on: ubuntu-latest
    if: false
    steps:
      - run: echo Hello world! && exit 1
```