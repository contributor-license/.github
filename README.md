# .github

Organization-level GitHub configuration for
[contributor-license](https://github.com/contributor-license). Nothing here is
part of any product.

| Path | Effect |
| --- | --- |
| [`profile/README.md`](profile/README.md) | Renders as the organization landing page at [github.com/contributor-license](https://github.com/contributor-license) |
| `profile/logo-light.png`, `profile/logo-dark.png` | Logo pair for that page. Served via `prefers-color-scheme` because the navy is unreadable on a dark background |
| `CODE_OF_CONDUCT.md` | Default for every repository without its own |
| `CONTRIBUTING.md` | Default for every repository without its own |
| `SECURITY.md` | Default for every repository without its own |
| `SUPPORT.md` | Default for every repository without its own |
| `.github/ISSUE_TEMPLATE/config.yml` | Default issue routing |

## How the defaults work

Files in the root are inherited by any repository in the organization that does
not publish its own copy. A repository with its own file always wins — for
instance [cla-action](https://github.com/contributor-license/cla-action) has a
more specific `SECURITY.md` covering the `pull_request_target` threat model, and
that is the one that applies there.

So keep the files here general. Anything specific to one project belongs in that
project.

## Editing the organization page

`profile/README.md` is the org landing page. Two things to know:

- This repository must stay **public**. GitHub ignores `profile/README.md` in a
  private `.github` repository, and the org page silently goes blank.
- Image paths in it are relative to `profile/`.

## Brand assets

Logo sources and generated PNGs live in
[docs/brand](https://github.com/contributor-license/docs/tree/main/brand), not
here. The two images in `profile/` are copies sized for this page.
