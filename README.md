# setup-pre-commit action

easy way to install [pre-commit](https://pre-commit.com/) in your GitHub Actions
workflows.

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@9c091bb21b7c1c1d1991bb908d89e4e9dddfe3e0  # v7.0.0
      - uses: pcrockett/setup-pre-commit@LATEST_RELEASE_TAG
```

if you don't want to use the default version of pre-commit that comes with this action, you
can specify your own version and checksum:

```yaml
- uses: pcrockett/setup-pre-commit@LATEST_RELEASE_TAG
  with:
    version: '4.6.0'
    checksum: 'ea8a0c84902e48c1875558f2f362ed8476773aa5fc8c16c5d8f2acc2a2830a65'
```

**recommended:** run [pinact](https://github.com/suzuki-shunsuke/pinact) to pin your
actions to a specific release. don't worry, if you're using Dependabot, Renovate, etc.,
they will update your pins correctly for you.

```bash
pinact run --update
```
