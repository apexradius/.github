# GitHub organization metadata - Architecture

## Purpose

| Question | Answer |
| --- | --- |
| Whom? | Metadata maintainers. |
| What? | GitHub-consumed Markdown surfaces. |
| Where? | This owning project, `docs/workflow/ARCHITECTURE.md`, and the linked canonical sources below. |
| Why it exists? | Apply github-consumed markdown surfaces to present Apex Radius clearly and give contributors appropriate community defaults. |
| Why this approach? | Use standard GitHub Markdown surfaces and current company facts while keeping policy in ApexOS. |
| Why it matters? | An agent can update public identity without inventing software architecture or unsupported commitments. |

`profile/README.md` is the organization-facing presentation source. Root CONTRIBUTING, SECURITY and CODE_OF_CONDUCT provide default community material where GitHub inheritance applies; repository-specific files may take precedence. This task inspected source, not every organization's current default resolution.

README and `docs/architecture.md` explain the repository to maintainers. There is no build system, API backend or deployment artifact. GitHub's rendering/default consumption is the external service boundary, and its live state must be observed separately from local edits.

## Continue

Return to [INDEX.md](../../INDEX.md) and finish all routes relevant to the latest task before acting. After verification, update affected owning facts, REPORT and HANDOFFS.
