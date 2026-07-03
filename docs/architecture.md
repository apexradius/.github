# Architecture

The `.github` repository is a GitHub metadata repo. It does not ship software; it supplies
organization-level presentation and optional default community files.

## Component Map

```mermaid
flowchart TD
    Org[apexradius org] --> Metadata[.github repo]
    Metadata --> Profile[profile/README.md]
    Metadata --> Community[community defaults]
    Profile --> OrgPage[GitHub org page]
    Community --> NewIssues[Issue and PR defaults]
    Community --> RepoStandards[Repo contribution defaults]
```

## Update Sequence

```mermaid
sequenceDiagram
    actor Maintainer
    participant Repo as .github repo
    participant GitHub as GitHub
    participant Public as Org profile

    Maintainer->>Repo: Edit profile/README.md
    Maintainer->>Repo: Run whitespace and secret checks
    Maintainer->>GitHub: Push main
    GitHub->>Public: Render updated profile
```

## Rules

- Keep profile copy concise and public-safe.
- Do not include secrets, private client details, or operational runbooks.
- Put repo-wide standards in Apex_Core; keep this repo focused on GitHub metadata.
