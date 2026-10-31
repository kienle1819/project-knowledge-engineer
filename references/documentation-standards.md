# Documentation Standards

## General rules

- Write concise, technical English by default.
- Keep one canonical home for each fact; link rather than duplicate.
- Prefer exact paths, symbol names, configuration keys, and executable commands.
- Verify every implementation claim against source, tests, schemas, or deployment configuration.
- Label uncertainty: `Verified`, `Inferred`, `Proposed`, or `Needs verification`.
- Do not document secrets, tokens, private keys, credentials, or sensitive personal data.
- Avoid timestamps and conversation history unless they are operationally relevant.
- Update indexes and cross-references whenever files are added, renamed, or removed.

## Recommended document metadata

Where useful, include:
- Purpose
- Scope
- Status
- Last verified (date, only if maintained reliably)
- Related documents

Do not add metadata that the repository cannot keep accurate.

## Workflow document

A workflow doc should explain trigger, entry point, sequence, files/symbols, dependencies, configuration, commands, side effects, failure modes, and verification.

## Project specification

A project spec should describe the current implementation, not an aspirational target. Separate current state from planned changes.

## Memory document

Store discoveries that would otherwise require expensive rediscovery: root causes, non-obvious behavior, compatibility caveats, debugging methods, and failed approaches.

## Principle document

Store durable rules that future contributors or agents should follow. Each principle should include rationale and scope. Avoid generic platitudes.
