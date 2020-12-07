# GitHubActions-test

test simple Github actions workflows.
## Greetings workflow

## Comment on new PRs workflow
name: Greetings

on: [pull_request, issues]

jobs:
  greeting:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/first-interaction@v1
      with:
        repo-token: ${{ secrets.GITHUB_TOKEN }}
        issue-message: 'Hello there!'
        pr-message: 'Hello there'
