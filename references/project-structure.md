# Project Knowledge Structure

Use this structure for a new knowledge base, adapting to existing repository conventions:

```text
AGENTS.md
CLAUDE.md
README.md
docs/
├── README.md
├── workflow/
│   ├── README.md
│   └── <capability>.md
├── project/
│   ├── README.md
│   └── <topic>.md
├── memory/
│   ├── README.md
│   └── <topic>.md
└── principle/
    ├── README.md
    └── <topic>.md
```

## Ownership

- `AGENTS.md`: shared repository instructions for coding agents.
- `CLAUDE.md`: Claude-specific instructions and integrations; refer to shared rules.
- `docs/README.md`: navigation and knowledge-base conventions.
- Each subfolder README: index of canonical documents in that category.

## Naming

Use descriptive, stable, lowercase kebab-case filenames. Prefer capability or topic names over dates. Use dates only when the information is inherently time-bound, such as incident reports.
