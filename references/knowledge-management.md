# Knowledge Management

## Choose the right destination

| Information | Destination |
|---|---|
| How to execute a feature or operational process | `docs/workflow/` |
| What the system contains and how it is structured | `docs/project/` |
| Non-obvious discoveries and lessons | `docs/memory/` |
| Reusable rules and constraints | `docs/principle/` |

## Update rather than duplicate

Before creating a document:
1. Search the relevant README index.
2. Search existing docs for the topic and key identifiers.
3. Update the canonical document if one exists.
4. Split a document only when it has distinct ownership or becomes difficult to navigate.
5. Add links from relevant indexes and related docs.

## Preserve confidence levels

- **Verified:** directly confirmed in source, tests, runtime output, or configuration.
- **Inferred:** strongly suggested by evidence but not directly confirmed.
- **Proposed:** a recommendation or intended future design.
- **Needs verification:** insufficient evidence.

Never describe a proposal as implemented.

## Knowledge freshness

Re-check paths, symbols, versions, commands, and config keys when using old docs. Treat documentation as a map, not as authority over the current implementation.

## Privacy and security

Never store secrets or raw credential-bearing output. Redact sensitive values. Do not copy entire logs when a short sanitized excerpt and root-cause explanation are sufficient.
