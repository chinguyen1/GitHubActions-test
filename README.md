# GitHubActions-test

test simple Github actions workflows.
## Greetings workflow

## Comment on new PRs workflow
````- name: 'Comment PR'
  uses: actions/github-script@0.3.0
  if: github.event_name == 'pull_request'
  with:
    github-token: ${{ secrets.WORKFLOW2 }}
    script: |
      const { issue: { number: issue_number }, repo: { owner, repo }  } = context;
      github.issues.createComment({ issue_number, owner, repo, body: 'You should expect an initial response to your PR from the team within 7 days. Note that this response may be delayed during holiday periods.' });````
