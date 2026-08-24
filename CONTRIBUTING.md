# Contributing to Simantic

Thanks for taking the time to contribute. This file applies to every repository
under [simantic-dev](https://github.com/simantic-dev) that does not have its
own `CONTRIBUTING.md`.

## What is open right now

Simantic is in alpha, and most of the platform — the simulation engines, the
MCU and peripheral models, and the board tooling — is still developed
privately. The repositories that are public and accept outside contributions
today are:

- [**pippy**](https://github.com/simantic-dev/pippy) — the `simantic` Python
  SDK and pytest plugin.
- [**crosspoint-reader**](https://github.com/simantic-dev/crosspoint-reader) —
  open-source e-reader firmware.
- [**homebrew-simantic**](https://github.com/simantic-dev/homebrew-simantic) —
  the Homebrew tap.

Issues are welcome on any public repository, whether or not you plan to send a
patch. Telling us which MCU or peripheral you need is genuinely useful.

## Before you write code

**Open an issue first for anything non-trivial.** A short description of the
problem and the approach you have in mind saves you from writing a patch we
cannot take — for example because it conflicts with something unreleased. For
an obvious bug fix or a typo, just send the pull request.

## Pull requests

- Branch from `main` and keep the change focused on one thing. A pull request
  that fixes a bug *and* reformats the file is hard to review.
- Match the style of the code around you, even where you would do it
  differently. Do not reformat code you are not otherwise changing.
- Add a test that fails before your change and passes after it. For a bug fix,
  that test is the most valuable part of the patch.
- Make sure the existing test suite passes locally, and keep CI green.
- Write commit messages in the imperative mood ("Fix CAN filter index", not
  "Fixed..."), with a body explaining *why* when the reason is not obvious.
- Fill in the pull request template so a reviewer can tell what changed and how
  it was verified.

## Reporting bugs

A good report includes:

- What you expected to happen, and what happened instead.
- The package or CLI version, your OS, and your Python version.
- The smallest script or firmware that reproduces it.
- The output of `simantic status`, when the issue involves the SDK or CLI.

Simulation bugs are usually reproducible by construction — if you have a run
that fails the same way every time, say so, and tell us the exact command.

## Licensing

Unless a repository says otherwise, contributions are accepted under that
repository's license (`pippy` is MIT). By opening a pull request you confirm
you have the right to contribute the code under those terms.

## Code of conduct

Participation is governed by our [Code of Conduct](CODE_OF_CONDUCT.md).
