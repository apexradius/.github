# GitHub organization metadata: project index

For product mission or accepted direction, consult [prompt.md](prompt.md). This index locates the existing project contracts; it does not authorize historical operations.

## Read when needed

Read only the documents needed for the current task. Use the task table below; do not traverse every dossier at startup.

- Resuming work: [HANDOFFS](docs/workflow/HANDOFFS.md).
- Implementation or verification: the affected source and [TESTING](docs/workflow/TESTING.md).
- Product-specific working constraints: [AGENTS](docs/workflow/AGENTS.md).
- Research/provenance: relevant [REFERENCES](docs/workflow/REFERENCES.md).

Commands, versions, dependencies, and directory layout should be read from their owning files when needed.

## Task routes

| Requested work | Owning contracts |
| --- | --- |
| Scope, requirements or priorities | [PRD](docs/workflow/PRD.md), [capabilities](docs/workflow/CAPABILITIES.md), [architecture](docs/workflow/ARCHITECTURE.md) |
| Component behavior or bug | [architecture](docs/workflow/ARCHITECTURE.md), [code style](docs/workflow/CODE_STYLE.md), [testing](docs/workflow/TESTING.md) |
| Interface or persistence | [API](docs/workflow/API.md), [database](docs/workflow/DATABASE.md), [security](docs/workflow/SECURITY.md) |
| Visible experience | [design](docs/workflow/DESIGN.md), [wireframes](docs/workflow/WIREFRAMES.md), [PRD](docs/workflow/PRD.md) |
| Configuration, operation or recovery | [security](docs/workflow/SECURITY.md), [secret locations](docs/workflow/SECRETS.md), [maintenance](docs/workflow/MAINTENANCE.md) |
| Resume or close a task | [handoff](docs/workflow/HANDOFFS.md), [report](docs/workflow/REPORT.md), [references](docs/workflow/REFERENCES.md) |

Combine all applicable routes; a security, data or release boundary adds its route even for a small UI edit. Non-applicable roles retain their stated reasons.

## Project source map

See [canonical public and company sources](docs/workflow/REFERENCES.md) for the original metadata source map, and [verification](docs/workflow/TESTING.md) for the document-checker interfaces.

## Domain glossary

| Term | Meaning in this project |
| --- | --- |
| Profile README | GitHub-rendered organization presentation. |
| Community default | Fallback contributor/security guidance, subject to repository overrides. |
| Source versus live | Markdown changes versus observed provider rendering. |

Definitions follow [ARCHITECTURE](docs/workflow/ARCHITECTURE.md); consult that owner for contracts and limitations.

## Review evidence

[Source-bound review continuity](docs/workflow/REVIEW.md) records scenario scope and limits.

## Completion

Use the latest user task and preserve unrelated work. Update affected facts and record verification and continuation. Navigation checks establish neither product readiness nor delivery or knowledge freshness.
