# Support

## Setting up the action

Start with the [cla-action README](https://github.com/contributor-license/cla-action#readme).
It covers the workflow file, every input, and the two inherited defaults that
catch people out — `path-to-signatures` and `branch` defaulting to `master`.

## Migrating from contributor-assistant/github-action

One line, and your existing signatures keep working. See
[Migrating](https://github.com/contributor-license/cla-action#migrating).
If something behaves differently from the original, that is a bug worth
reporting — open a
[compatibility issue](https://github.com/contributor-license/cla-action/issues/new?template=compatibility.yml).

## Questions

[Discussions](https://github.com/contributor-license/cla-action/discussions) for
questions and ideas.
[Issues](https://github.com/contributor-license/cla-action/issues) for bugs.

## Before reporting a bug

Several behaviours that look like bugs are replicated from the original action
on purpose, because changing them would break repositories migrating across.
They are catalogued in
[SPEC.md](https://github.com/contributor-license/cla-action/blob/main/SPEC.md) —
worth a look first.

## Not support

Whether a particular CLA text is right for your project is a legal question, not
a tooling one. The [CLA in cla-action](https://github.com/contributor-license/cla-action/blob/main/CLA.md)
is a reasonable starting shape, not legal advice.
