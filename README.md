# pull-request-summary

[![version](https://badgen.net/github/release/ai-action/pull-request-summary)](https://github.com/ai-action/pull-request-summary/releases)
[![test](https://github.com/ai-action/pull-request-summary/actions/workflows/test.yml/badge.svg)](https://github.com/ai-action/pull-request-summary/actions/workflows/test.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

📝 GitHub Action that summarizes pull requests with AI (LLM).

## Quick Start

```yaml
# .github/workflows/pr-summary.yml
on: pull_request
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

Append summary to PR description:

```yaml
- uses: ai-action/pull-request-summary@v1
```

See [action.yml](action.yml)

## Inputs

### `model`

**Optional**: The language [model](https://ollama.com/library) to use. Defaults to [codellama](https://ollama.com/library/codellama):

```yaml
- uses: ai-action/pull-request-summary@v1
  with:
    model: codellama
```

### `prompt`

**Optional**: The input prompt that comes before the PR diff. Defaults to:

```yaml
- uses: ai-action/pull-request-summary@v1
  with:
    prompt: 'Summarize the code diff concisely:'
```

### `token`

**Optional**: The GitHub token. Defaults to `GITHUB_TOKEN`:

```yaml
- uses: ai-action/pull-request-summary@v1
  with:
    token: ${{ secrets.GITHUB_TOKEN }}
```

## License

[MIT](LICENSE)
