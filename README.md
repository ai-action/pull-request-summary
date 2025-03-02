# pull-request-summary

[![version](https://badgen.net/github/release/ai-action/pull-request-summary)](https://github.com/ai-action/pull-request-summary/releases)
[![test](https://github.com/ai-action/pull-request-summary/actions/workflows/test.yml/badge.svg)](https://github.com/ai-action/pull-request-summary/actions/workflows/test.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

📝 GitHub Action that summarizes pull requests with AI (LLM).

## Quick Start

```yaml
# .github/workflows/pr-summary.yml
on: push
jobs:
  pr-summary:
    runs-on: ubuntu-latest
    permissions:
      contents: read
      pull-requests: write
    steps:
      - name: PR summary
        uses: ai-action/pull-request-summary@v1
```

## Usage

**Basic:**

```yaml
- uses: ai-action/pull-request-summary@v1
```

See [action.yml](action.yml)

## Inputs

### `version`

**Optional**: The version. Defaults to `1.2.3`:

```yaml
- uses: ai-action/pull-request-summary@v1
  with:
    version: 1.2.3
```

## License

[MIT](LICENSE)
