# Code Review Checklist

## Scope and Git state

- [ ] Inspect `git status --short`.
- [ ] Inspect unstaged and staged diffs separately.
- [ ] Identify untracked, renamed, and deleted files.
- [ ] Preserve unrelated user changes.
- [ ] Read relevant surrounding code and history where useful.

## Correctness

- [ ] Normal and edge-case behavior
- [ ] Null, empty, malformed, and out-of-range inputs
- [ ] Error handling and retry behavior
- [ ] Concurrency, async execution, race conditions
- [ ] Transaction and consistency boundaries
- [ ] Backward compatibility and regression risk

## Security

- [ ] Authentication and authorization
- [ ] Injection and unsafe query construction
- [ ] XSS, CSRF, SSRF, path traversal, deserialization as applicable
- [ ] Secret exposure and sensitive logging
- [ ] File, network, process, and cloud permissions
- [ ] Dependency and configuration risks

## Maintainability and architecture

- [ ] Dead, unreachable, or unused code
- [ ] Duplicate logic and unnecessary dependencies
- [ ] Resource leaks and lifecycle cleanup
- [ ] Module boundaries, dependency direction, coupling
- [ ] API, schema, and configuration consistency
- [ ] Complexity and scope discipline

## Tests and delivery

- [ ] Tests cover changed behavior and failure paths
- [ ] Build, lint, type checks, and tests run where applicable
- [ ] Migration and deployment risks considered
- [ ] Final diff reviewed after fixes
- [ ] No accidental secrets or unrelated modifications

## Severity

- `CRITICAL`: exploitable vulnerability, data loss, or severe outage likely.
- `HIGH`: major security, correctness, or availability issue.
- `MEDIUM`: meaningful defect or maintainability risk with bounded impact.
- `LOW`: minor issue, clarity improvement, or limited risk.

Always state whether a finding is introduced by the diff or pre-existing. Explain evidence and impact.
