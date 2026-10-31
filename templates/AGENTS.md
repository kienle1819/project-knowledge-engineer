# Repository Agent Instructions

## Knowledge-first policy

Before substantive work:
1. Read the root `README.md` and this file.
2. Read `CLAUDE.md` when applicable.
3. Read `docs/README.md` and the relevant README indexes under `docs/`.
4. Find and read relevant workflow, project, memory, and principle documents.
5. Verify the documented paths, symbols, and behavior against the current source.

## Execution policy

- Locate the exact implementation before editing.
- Follow established workflows and project conventions.
- Prefer updating canonical documentation over creating duplicates.
- Keep changes scoped to the user's request.
- Preserve unrelated and uncommitted user changes.
- Never invent implementation facts or claim checks passed unless executed.
- Never put secrets or credentials in source or documentation.
- Do not commit, push, deploy, run destructive commands, or apply migrations without explicit authorization.

## Knowledge layout

- `docs/workflow/`: execution procedures and operational workflows.
- `docs/project/`: architecture, modules, APIs, data, infrastructure, and configuration.
- `docs/memory/`: discoveries, root causes, caveats, and lessons.
- `docs/principle/`: durable engineering rules.

## Core loop

**Read Knowledge → Locate Implementation → Verify → Execute → Test → Preserve Knowledge**

Technical documentation should be clear English by default. User communication may follow the user's preferred language.
