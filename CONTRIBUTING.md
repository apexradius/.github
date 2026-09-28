# Contributing

Thanks for your interest in an Apex Radius project.

Each repository documents its own setup, standards, and workflow — start with
that repo's `README.md` and any `docs/` directory. Open an issue or pull
request against the specific repository you want to change; there is no central
contribution queue.

- Keep pull requests focused: one change per PR.
- Match the existing code style and structure of the repo you are touching.
- Describe what changed and why in the PR body.

For security issues, do not open a public issue — see [SECURITY.md](SECURITY.md).

## Publishing this metadata repository

Use a focused branch and pull request, not a direct push to `main`. Follow the
[verification guide](docs/workflow/TESTING.md), obtain independent review, and
merge only after clean AXI validation and exact-head CI without skips or overrides.
The delivery executor owns publication; documentation checks do not authorize it.
After approved publication, observe the affected GitHub rendering separately.
Recovery for a qualified merge is a reviewed revert PR, never a force reset.
