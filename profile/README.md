<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://simantic.dev/simantic_logo_4_full_transparent.png">
    <img src="https://simantic.dev/simantic_logo_4_inverted_full_transparent.png" alt="Simantic" width="360">
  </picture>
</p>

<h3 align="center">Test your firmware without a board.</h3>

<p align="center">
  <a href="https://simantic.dev">Website</a> ·
  <a href="https://simantic.dev/docs">Docs</a> ·
  <a href="https://pypi.org/project/simantic/">PyPI</a> ·
  <a href="https://simantic.dev/pricing">Pricing</a> ·
  <a href="https://simantic.dev/apply">Careers</a>
</p>

---

Simantic runs your real firmware binary on a simulated microcontroller — the
core, the peripherals, and the things wired to them. Nothing to plug in,
nothing to flash, no probe on the desk.

Because the whole machine is software, you can do things a bench cannot:

- **See inside.** Read any variable, register, or RTOS thread while the
  firmware runs, without halting it.
- **Poke it.** Press buttons, send CAN frames, feed a radio — from a script.
- **Repeat exactly.** Time advances only when you ask, so a run comes out the
  same on your laptop and in CI.

## Try it

```bash
pip install simantic
```

```python
from simantic import Sim

with Sim(elf="fw.elf", mcu="STM32F401RE", uart="usart2") as sim:
    sim.expect("ready")
    sim.inject_gpio("gpioc", 13, True)      # press the user button
    sim.expect("button pressed")
    assert sim.read_u32("press_count") == 1
```

That is a whole test — no probe, no breakpoint, no waiting on hardware. The
simulator runs inside your Python process, so there is no server to start.

> The Python SDK is **alpha (0.3.x)** and the API can still change without a
> deprecation period. Pin an exact version if you depend on it, and tell us
> what breaks.

## What's public

| Repository | What it is |
| --- | --- |
| [**pippy**](https://github.com/simantic-dev/pippy) | The `simantic` Python SDK and pytest plugin — [on PyPI](https://pypi.org/project/simantic/). MIT. |
| [**homebrew-simantic**](https://github.com/simantic-dev/homebrew-simantic) | Homebrew tap for the `sim` CLI: `brew tap simantic-dev/simantic && brew install simantic`. |
| [**crosspoint-reader**](https://github.com/simantic-dev/crosspoint-reader) | Open-source e-reader firmware for the Xteink X3/X4 — and a real target we simulate. |

Most of the platform — the simulation engines, the MCU and peripheral models,
and the board tooling — is still developed privately while we are in alpha.
Documentation for those parts is at [simantic.dev/docs](https://simantic.dev/docs).

## Get in touch

- **Questions and bug reports** — open an issue on the relevant repository.
- **Security issues** — see our [security policy](https://github.com/simantic-dev/.github/blob/main/SECURITY.md). Please do not open a public issue.
- **Everything else** — email `founders@simantic.dev`.

We are hiring: [open roles](https://www.ycombinator.com/companies/simantic/jobs).

<p align="center">
  <sub>Simantic, Inc. · <a href="https://simantic.dev">simantic.dev</a> · <a href="https://www.linkedin.com/company/simantic">LinkedIn</a></sub>
</p>
