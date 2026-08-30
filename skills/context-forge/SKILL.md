---
name: context-forge
description: Grill out-of-code product context into context/*.md.
disable-model-invocation: true
---

Read [references/grilling.md](references/grilling.md) and run it. The tree is the product in the world, not the codebase.

# Context forge

Capture what the repo does not confess. One product. Create a file on its first fact; skip empty files.

## After each round

Write what landed. Then grill the new frontier. Do not implement the product in this session.


| File                    | Holds                                                                                                       |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| `context/PRODUCT.md`    | Who it is for, what “good” is, who is not a customer, and ADRs (choices you are keeping)                    |
| `context/OPERATIONS.md` | How it actually runs, including unwritten environment. Omit anything CI, Docker, or `--help` already states |
| `context/TRUST.md`      | Trust boundaries, data class, who may act                                                                   |
| `context/CONTEXT.md`    | Glossary - names, not implementation                                                                        |


Point at where secrets live. Never paste tokens, passwords, or keys into these files.

Finding facts (filesystem, tools, docs) is your job. Decisions are the user's. The session is done when the frontier is empty and the user confirms the capture matches.