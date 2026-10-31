# Project Knowledge Engineer

A reusable Agent Skill for maintaining verified project knowledge across the software development lifecycle.

It combines three recurring lifecycle activities:

- **P0 — Initialize:** establish project instructions and a navigable knowledge base once.
- **P1 — Update knowledge:** capture durable workflow and implementation knowledge after meaningful work.
- **P2 — Pre-commit review:** inspect diffs, identify risks, run appropriate checks, and extract reusable lessons.

It also supports workflow discovery, documentation synchronization, and knowledge-base audits.

## Why use a Skill?

The Skill contains reusable procedures and detailed checklists that an agent can load when relevant. Keep `AGENTS.md` and `CLAUDE.md` in the repository: they provide persistent project-level instructions. The Skill complements those files; it does not replace them.

## Contents

```text
project-knowledge-engineer/
├── SKILL.md
├── README.md
├── references/
│   ├── documentation-standards.md
│   ├── knowledge-management.md
│   ├── code-review-checklist.md
│   └── project-structure.md
└── templates/
    ├── AGENTS.md
    ├── CLAUDE.md
    ├── docs-readme.md
    ├── workflow-template.md
    ├── project-spec-template.md
    ├── memory-template.md
    └── principle-template.md
```

## Install

Copy the `project-knowledge-engineer/` directory into the skill directory supported by your coding agent.

### Claude Code

```bash
mkdir -p .claude/skills
cp -R project-knowledge-engineer .claude/skills/
```

### Codex

```bash
mkdir -p .agents/skills
cp -R project-knowledge-engineer .agents/skills/
```

### Gemini CLI / Antigravity / other agents

Use the Agent Skills directory and discovery mechanism supported by the installed version of the agent. Skill discovery conventions can vary by product and release; verify the current product documentation rather than assuming one universal path.

## Usage examples

Ask your agent naturally:

- "Initialize this repository's project knowledge base."
- "After this task, update the workflow and project docs with verified implementation details."
- "Trace and document the complete authentication workflow."
- "Review the current Git diff before commit, fix clear issues, and update engineering memory."
- "Audit the docs for stale paths, duplicated guidance, and missing workflows."

If slash-command invocation is supported by the agent, it may expose the Skill by its name. Natural-language triggering is also supported when the agent's skill discovery works.

## Recommended lifecycle

```text
P0 Initialize (once)
       |
       v
Read knowledge -> Locate implementation -> Verify source
       |                                  |
       v                                  v
Implement / investigate -> Test -> P1 Update knowledge
                                      |
                                      v
                           P2 Pre-commit review
                                      |
                           READY / warnings / not ready
```

P1 should happen after meaningful work, not after every trivial chat. P2 should happen before each intended commit or whenever a diff review is requested.

## Documentation layout created in target projects

```text
docs/
├── README.md
├── workflow/
│   └── README.md
├── project/
│   └── README.md
├── memory/
│   └── README.md
└── principle/
    └── README.md
```

## Language

The Skill's instructions and templates are English-first for consistency across coding agents. The agent can communicate with the user in Vietnamese or another preferred language. Preserve exact source identifiers, command names, and domain terminology.

## Safety

The Skill instructs agents to preserve unrelated changes, avoid secrets in docs, verify claims against source, report tests honestly, and avoid commit/push/deploy/destructive actions without explicit authorization.

## Customize

Adapt the templates to your repository's stack and compliance needs. Do not force the standard folder layout onto a repository that already has a coherent documentation structure.
