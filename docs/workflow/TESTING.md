# GitHub organization metadata - Testing

## Purpose

| Question | Answer |
| --- | --- |
| Whom? | Reviewers. |
| What? | Source quality and rendered acceptance. |
| Where? | This owning project, `docs/workflow/TESTING.md`, and the linked canonical sources below. |
| Why it exists? | Apply source quality and rendered acceptance to present Apex Radius clearly and give contributors appropriate community defaults. |
| Why this approach? | Use standard GitHub Markdown surfaces and current company facts while keeping policy in ApexOS. |
| Why it matters? | An agent can update public identity without inventing software architecture or unsupported commitments. |

For a content change, check factual provenance, Markdown links, whitespace and an appropriately scoped redacted secret scan. After authorized publication, inspect the actual organization profile or affected default document. Local source checks cannot prove GitHub displayed the intended revision. No live profile/mailbox check ran in this reconstruction.

## Local checks

Run from the repository root with Python 3.10 or newer, as required by the
pinned CommonMark parser. The navigation checks use it to distinguish rendered
links and headings from code examples. There is no application build or
configured general-purpose formatter/linter.

Create and activate a repository-local virtual environment, then install the
pinned validation dependencies before running either checker or their fixtures.
CI installs the same pins.

```bash
python3 -m venv .venv
. .venv/bin/activate
python -m pip install -r tools/requirements-workflow.txt
```

Static documentation and hygiene checks:

```bash
git diff --check
python3 tools/check_workflow.py --tracked
python3 tools/check_review.py
gitleaks detect --source . --no-banner --redact
```

Gitleaks must already be available on PATH; report an unavailable scan rather
than claiming it passed. Its redacted output must not be replaced with secret values.
For committed changes, give `git diff --check` the reviewed base and candidate revisions.

`check_workflow.py [root] [--tracked] [--budget WORDS]` checks the required
workflow files, local navigation and a default 3,500-word core reading budget.
`--tracked` also checks that linked files are tracked or staged. It does not fetch
external links, inspect live GitHub rendering, or establish agent comprehension.

`check_review.py [root]` checks the review snapshot's shape, file hashes,
entrypoint link and completion/status consistency. After inspecting a changed
reviewed file, regenerate its SHA256 in `review.json`; never refresh hashes just
to hide stale review. Keep stage outcomes tied to their actual evidence. The
historical baseline hashes in REVIEW.md are not current-candidate hashes.

The Test phase separately runs the behavioral checker fixtures:

```bash
python3 -m unittest discover -s tools -p 'test_*check.py'
```

[Project context CI](../../.github/workflows/project-context.yml) runs both document
checkers and these fixtures on pull requests and pushes to `main` or `master`.
A consistent pending review snapshot is not evidence that delivery is complete.

## Continue

Return to [INDEX.md](../../INDEX.md) and finish all routes relevant to the latest task before acting. After verification, update affected owning facts, REPORT and HANDOFFS.
