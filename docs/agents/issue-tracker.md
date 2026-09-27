# Issue tracker: GitHub

GitHub Issues are the engineering work tracker for `looksawful/openclaw`.

## Harness and tool choice

GitHub Issues are the source of truth, not a particular client. GPT/OpenClo should use an authenticated GitHub connector/API when available; an authenticated `gh` CLI inside the repository clone is equivalent. Do not create a parallel local tracker merely because one client is unavailable.

## Conventions

Create, read, list, comment on, label, assign and close work in GitHub Issues. Read body, comments and current labels together. Resolve whether a bare `#<number>` is an issue or PR before mutating it.

## Pull requests as a triage surface

PRs as a request surface: no.

## Skill operations

- Publish to the issue tracker: create a GitHub issue.
- Fetch the relevant ticket: read the issue including comments and labels.
- Apply/remove triage roles through `docs/agents/triage-labels.md`.

## Wayfinding operations

- Map: one issue labelled `wayfinder:map` with Notes / Decisions-so-far / Fog.
- Child: GitHub sub-issue when available; otherwise map task-list link plus `Part of #<map>`.
- Types: `wayfinder:research`, `wayfinder:prototype`, `wayfinder:grilling`, `wayfinder:task`.
- Blocking: native issue dependencies when available; otherwise leading `Blocked by: #<n>` metadata.
- Frontier: first open child in map order with no open blocker and no assignee.
- Claim: assign the ticket to the current operator.
- Resolve: post durable evidence, close the child, and record the resulting decision/context pointer on the map.
