# Security policy

Applies to every repository in the `contributor-license` organisation that does
not publish its own policy. `cla-action` has
[its own](https://github.com/contributor-license/cla-action/blob/main/SECURITY.md),
which is more specific and takes precedence.

## Reporting

Report privately through
[GitHub Security Advisories](https://github.com/contributor-license/cla-action/security/advisories/new),
or email anthony@linsday.net.

Do not open a public issue for a security problem.

Expect an acknowledgement within a few days. Fixes ship in a patch release and
the advisory is published with credit, unless you would rather not be named.

## What we care about most

This organisation builds tooling that repositories grant write access to, and
that records agreements people are held to. Two classes of problem outrank
everything else:

- **Privilege escalation through a workflow.** Anything that lets a pull request
  author reach a write-scoped token or a repository secret.
- **Signature integrity.** Anything that records a signature for someone who did
  not give one, or removes or alters one that was given.

Report those even if you are unsure they are exploitable.
