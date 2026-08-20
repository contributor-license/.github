<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="logo-dark.png">
    <source media="(prefers-color-scheme: light)" srcset="logo-light.png">
    <img alt="Contributor License" src="logo-light.png" width="140">
  </picture>
</p>

<h1 align="center">Contributor License</h1>

<p align="center">
  Automated CLA and DCO signing for pull requests.<br>
  Contributors sign in the PR; signatures are recorded in your own repository
  and re-checked on every commit.
</p>

---

## Projects

| | |
| --- | --- |
| **[cla-action](https://github.com/contributor-license/cla-action)** | GitHub Action. CLA and DCO checks on pull requests, signatures stored in your repository. **Available now.** |
| **app** | Hosted service — dashboard and org-wide management, for teams who would rather not run it themselves. *In development.* |
| **[docs](https://github.com/contributor-license/docs)** | Documentation and brand assets. |

## Quick start

```yaml
- uses: contributor-license/cla-action@v1
  env:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  with:
    path-to-signatures: signatures/version1/cla.json
    path-to-document: https://github.com/<org>/<repo>/blob/main/CLA.md
    branch: main
    allowlist: dependabot[bot],bot*
```

Full workflow and inputs: [cla-action README](https://github.com/contributor-license/cla-action#readme).

## Moving from contributor-assistant/github-action

That project was [archived on 2026-08-06](https://github.com/contributor-assistant/github-action)
and its maintainer invited the community to continue it. `cla-action` is a
drop-in replacement. Migration is one line:

```diff
-      - uses: contributor-assistant/github-action@v2.6.1
+      - uses: contributor-license/cla-action@v1
```

Your existing signature file keeps working, nobody re-signs, and the bot adopts
its previous comment on each open pull request rather than posting a duplicate.
Behaviour is replicated deliberately, including several inherited quirks, and
every intentional difference is written down in
[SPEC.md](https://github.com/contributor-license/cla-action/blob/main/SPEC.md).

Not affiliated with or endorsed by SAP SE. `cla-action` is derived from their
Apache-2.0 work, with the original history preserved and attributed.

## Why signatures live in your repository

A CLA signature is a legal record. Keeping it in your own repository means:

- You can read, audit and back it up without asking anyone.
- No third party can lose it, hold it hostage, or go quiet on you.
- Nobody else becomes a processor of your contributors' personal data.

That property is not going away. The hosted service will be an option for teams
that want a dashboard, never a requirement.

## Security

`cla-action` runs on `pull_request_target` with a write-scoped token, because it
must comment on and commit for pull requests from forks. If you are wiring it up,
read the
[security policy](https://github.com/contributor-license/cla-action/blob/main/SECURITY.md)
first — particularly the part about never checking out pull request code in that
workflow.

Report vulnerabilities privately via
[Security Advisories](https://github.com/contributor-license/cla-action/security/advisories/new).

## Contributing

Issues and pull requests welcome. See
[CONTRIBUTING.md](https://github.com/contributor-license/cla-action/blob/main/CONTRIBUTING.md).
These repositories check their own pull requests with their own action.
