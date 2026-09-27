# Domain docs

How engineering skills should consume this repository's domain documentation.

Layout: **multi-context**.

## Before exploring, read these when present

- Start with root `CONTEXT-MAP.md`.
- Follow it only to the `CONTEXT.md` files relevant to the task.
- Read relevant system-wide ADRs under root `docs/adr/`.
- Read context-scoped ADRs beside the owning context when present.

If a context file or ADR directory named by the layout does not exist yet, proceed silently. Do not create empty placeholders up front. `/domain-modeling` creates or extends domain docs lazily when real terms or durable decisions are resolved.

## Consumer rules

- Use vocabulary from the owning context instead of inventing synonyms.
- Keep system-wide decisions in the root decision layer and context-specific decisions with the owning context.
- Surface ADR conflicts explicitly instead of silently overriding them.
- Repository-local policy and agent instructions override generic domain guidance.
