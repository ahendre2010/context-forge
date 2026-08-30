# Context Forge

An agent skill for capturing the product context that source code cannot: goals, operational knowledge, trust boundaries, terminology, and durable decisions.

Context Forge interviews you in focused rounds, verifies facts from the repository, and records only the context that is not already expressed by code or tooling. It does not implement the product.

## What it creates

The skill writes relevant findings to a `context/` directory:

| File | Contents |
| --- | --- |
| `PRODUCT.md` | Audience, success criteria, exclusions, and architectural decisions |
| `OPERATIONS.md` | Unwritten knowledge about how the product actually runs |
| `TRUST.md` | Trust boundaries, data classifications, and authorization |
| `CONTEXT.md` | Domain terminology and glossary entries |

Files are created only when there is something useful to record. Secrets are referenced by location, never copied into the context files.

## Usage

Install the [`skills/context-forge`](skills/context-forge) directory in your agent's skills directory, then invoke `context-forge` explicitly. The skill will:

1. Inspect the repository for facts it can discover itself.
2. Ask decision-focused questions in rounds.
3. Write confirmed context after each round.
4. Continue until no unanswered decisions remain and you confirm the result.

## License

[MIT](LICENSE)
