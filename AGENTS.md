# Agent instructions

Instructions for coding agents working in this repository. The lab's cross-repo map and shared
conventions live in [`ecohydro/uav`](https://github.com/ecohydro/uav).

## Decisions and reviews (posted to Slack)

Issues, pull requests and reviews in the lab's UAV repos post to the #canoply channel in the WAVES
Slack, where Kelly, Bryn and Shadman follow the work. Put decisions and reviews on GitHub so they
show up there, not only in your session.

**Decisions reserved for the user.** When you reach a decision that belongs to the user (product
scope; data formats, CLI flags or APIs other people use; anything that deletes data or writes to
real flight data; licences and paid tools), open an issue as well as asking in your session:

```bash
gh issue list -R ecohydro/uav --label needs-decision    # check it isn't already open
gh issue create -R ecohydro/uav --label needs-decision \
  --title "[cloudcompy_treeai] Decision: <the question in one line>" --body-file <file>
```

This repo has issues turned off, so its decision issues go in `ecohydro/uav` with `[cloudcompy_treeai]` at the start of the title.

Write the body for someone who hasn't seen your session: what you were working on (feature, branch,
spec path), the question, the options with their trade-offs, your recommendation, and what waits on
the answer. Ask one question per issue, and link the issue when you ask in the session.

- If the user answers in the session, post the answer as a comment and close the issue. The closed
  issue is the record of the decision.
- If work can't go on until it's answered, add the `blocked` label and leave the issue open.
- Cite the issue number where the decision is applied: the spec, `run-state.md`, or the PR
  description.
- Questions that span repos, or that touch the shared contracts, go in `ecohydro/uav`.

**Pull requests.** `.github/CODEOWNERS` asks Kelly, Bryn and Shadman for review (GitHub skips the
author). When you open a PR for finished work, open it ready for review, not as a draft, so the
review request goes out. In the description, list the decisions made along the way with links to
their issues, and anything a reviewer should check by hand.
