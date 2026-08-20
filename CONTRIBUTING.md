# Contributing

Applies across the `contributor-license` organisation. Repositories with their
own `CONTRIBUTING.md` — such as
[cla-action](https://github.com/contributor-license/cla-action/blob/main/CONTRIBUTING.md) —
take precedence.

## Before opening a pull request

- One change per pull request, and say what you tested it against.
- Add tests. A compatibility claim without a test is not a claim.
- Sign the CLA by commenting on your pull request:
  `I have read the CLA Document and I hereby sign the CLA`

These repositories gate their own pull requests with their own action, so a
broken change tends to announce itself.

## Compatibility comes first

`cla-action` v1 is a drop-in replacement for an archived project that
repositories depend on today. Anything that changes observable behaviour has to
be opt-in, documented in `SPEC.md`, and called out in the release notes. That
constraint is deliberate and it is not negotiable for v1.

## Contribution terms

Contributions are accepted under the
[CLA](https://github.com/contributor-license/cla-action/blob/main/CLA.md). You
keep your copyright; the grant is broad enough that the project can be offered
under separate commercial terms.
