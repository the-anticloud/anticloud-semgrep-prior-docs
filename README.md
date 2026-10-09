# SEMGREP PRIOR DOCS

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-software_development-lightgrey)

> Anticloud-hardened packaging of the upstream project `SEMGREP_PRIOR_DOCS` in category **SOFTWARE DEVELOPMENT**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** SOFTWARE DEVELOPMENT · **Upstream:** https://github.com/semgrep/semgrep · **Upstream pin:** `31729a1719c6e76ac8d41ec8fb9ab191621ee10f` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

<br />
<p align="center">
  <a href="https://semgrep.dev">
    <picture>
      <source media="(prefers-color-scheme: light)" srcset="images/semgrep-logo-light.svg">
      <source media="(prefers-color-scheme: dark)" srcset="images/semgrep-logo-dark.svg">
      <img src="https://raw.githubusercontent.com/semgrep/semgrep/develop/images/semgrep-logo-light.svg" height="100" alt="Semgrep logo"/>
    </picture>
  </a>
</p>
<h2 align="center">
  Code scanning at ludicrous speed.
</h2>
<p align="center">
  <a href="https://formulae.brew.sh/formula/semgrep">
    <img src="https://img.shields.io/homebrew/v/semgrep?style=flat-square" alt="Homebrew" />
  </a>
  <a href="https://pypi.org/project/semgrep/">
    <img alt="PyPI" src="https://img.shields.io/pypi/v/semgrep?style=flat-square&color=blue">
  </a>
  <a href="https://semgrep.dev/docs/">
      <img src="https://img.shields.io/badge/docs-semgrep.dev-purple?style=flat-square" alt="Documentation" />
  </a>
  <a href="https://go.semgrep.dev/slack">
    <img src="https://img.shields.io/badge/slack-3.5k%20members-green?style=flat-square" alt="Join Semgrep community Slack" />
  </a>
  <a href="https://github.com/semgrep/semgrep/issues/new/choose">
    <img src="https://img.shields.io/badge/issues-welcome-green?style=flat-square" alt="Issues welcome!" />
  </a>
  <a href="https://github.com/semgrep/semgrep#readme">
    <img src="https://img.shields.io/github/stars/semgrep/semgrep?label=GitHub%20Stars&style=flat-square" alt="Star Semgrep on GitHub" />
  </a>
  <a href="https://hub.docker.com/r/semgrep/semgrep">
    <img src="https://img.shields.io/docker/pulls/semgrep/semgrep.svg?style=flat-square" alt="Docker Pulls" />
  </a>
  <a href="https://hub.docker.com/r/semgrep/semgrep">
    <img src="https://img.shields.io/docker/pulls/semgrep/semgrep.svg?style=flat-square" alt="Docker Pulls (Old)" />
  </a>
  <a href="https://twitter.com/intent/follow?screen_name=semgrep">
    <img src="https://img.shields.io/twitter/follow/semgrep?label=Follow%20semgrep&style=social&color=blue" alt="Follow @semgrep on Twitter" />
  </a>
</p>
</br>

Semgrep is a fast, open-source, static analysis tool that searches code, finds bugs, and enforces secure guardrails and coding standards. Semgrep [supports 30+ languages](#language-support) and can run in an IDE, as a pre-commit check, and as part of CI/CD workflows.

Semgrep is semantic grep for code. While running `grep "2"` would only match the exact string _2_, Semgrep would [match `x = 1; y = x + 1` when searching for _2_](https://semgrep.dev/playground/s/5rKgj). Semgrep rules look like the code you already write; no abstract syntax trees, regex wrestling, or painful DSLs.

Note that in security contexts, Semgrep Community Edition will miss many true positives as it can only analyze code within the boundaries of a single function or file. If you want to use Semgrep for security purposes (**SAST**, **SCA**, or **secrets scanning**), the Semgrep AppSec Platform is strongly recommended since it adds the following critical capabilities:

1. Improved core analysis capabilities (cross-file, cross-function, data-flow reachability) that greatly reduce false positives by 25% and increase detected true positives by 250%
2. Contextual post-processing of findings with Semgrep Assistant (AI) to further reduce noise by [~20%](https://a.storyblok.com/f/151984/x/2d12dc0223/whitepaper_-ai-powered-appsec-engineer-automate.pdf?cv=1728584410408).  In addition, Assistant enriches findings with tailored, step-by-step remediation guidance that humans find actionable >80% of the time.
3. Customizable policies and seamless integration into developer workflows, giving security teams granular control over where, when, and how different findings are presented to developers (IDE, PR comment, etc.)

The Semgrep AppSec Platform works out-of-the-box with 20000+ proprietary rules across SAST, SCA, and secrets. Pro rules are written and maintained by the Semgrep security research team and are highly accurate, meaning AppSec teams can feel confident bringing findings directly to developers without slowing them down.

Semgrep analyzes code locally on your computer or in your build environment: **by default, code is never uploaded**. [Get started →.](#getting-started-)

<a href="#option-1-getting-started-from-the-cli">
<img src="https://raw.githubusercontent.com/semgrep/semgrep/develop/images/semgrep-scan-cli.jpg" alt="Semgrep CLI image"/></a>

### Language support

**Semgrep Code** supports 30+ languages, including:

Apex · Bash · C · C++ · C# · Clojure · Dart · Dockerfile · Elixir · HTML · Go · Java · JavaScript · JSX · JSON · Julia · Jsonnet · Kotlin · Lisp · Lua · OCaml · PHP · Python · R · Ruby · Rust · Scala · Scheme · Solidity · Swift · Terraform · TypeScript · TSX · YAML · XML · Generic (ERB, Jinja, etc.)

**Semgrep Supply Chain** supports 12 languages across 15 package managers, including:

C# (NuGet) · Dart (Pub) · Go (Go modules, `go mod`) · Java (Gradle, Maven) · Javascript/Typescript (npm, Yarn, Yarn 2, Yarn 3, pnpm) · Kotlin (Gradle, Maven) · PHP (Composer) · Python (pip, pip-tool, Pipenv, Poetry) · Ruby (RubyGems) · Rust (Cargo) · Scala (Maven) · Swift (SwiftPM)

For more information, see [Supported languages](https://semgrep.dev/docs/supported-languages/).

### Getting started 🚀

1. [From the Semgrep AppSec Platform](#option-1-getting-started-from-the-semgrep-appsec-platform-recommended)
2. [From the CLI](#option-2-getting-started-from-the-cli)

For new users, we recommend starting with the [Semgrep AppSec Platform](#option-1-getting-started-from-the-semgrep-appsec-platform-recommended) because it provides a visual interface, a demo project, result triaging and exploration workflows, and makes setup in CI/CD fast. Scans are still local and code isn't uploaded. Alternatively, you can also start with the CLI and navigate the terminal output to run one-off searches.

### Option 1: Getting started from the Semgrep Appsec Platform (Recommended)

<a hr

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **C/C++ / Make** (manifests: Makefile; scanned in UPSTREAM_CLONE)
- Top-level source layout: `changelog.d/`, `cli/`
- Snapshot size: **552 files**, **52010 lines of code** (measured; see Benchmarks)
- Primary languages: `.json` (167), `.py` (150), `.txt` (110), `.pyi` (35), `(none)` (31), `.md` (11)
- Upstream commit pinned for this packaging: `31729a1719c6e76ac8d41ec8fb9ab191621ee10f`

---

## Installation

<a href="#option-1-getting-started-from-the-cli">
<img src="https://raw.githubusercontent.com/semgrep/semgrep/develop/images/semgrep-scan-cli.jpg" alt="Semgrep CLI image"/></a>

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

1. Improved core analysis capabilities (cross-file, cross-function, data-flow reachability) that greatly reduce false positives by 25% and increase detected true positives by 250%
2. Contextual post-processing of findings with Semgrep Assistant (AI) to further reduce noise by [~20%](https://a.storyblok.com/f/151984/x/2d12dc0223/whitepaper_-ai-powered-appsec-engineer-automate.pdf?cv=1728584410408).  In addition, Assistant enriches findings with tailored, step-by-step remediation guidance that humans find actionable >80% of the time.
3. Customizable policies and seamless integration into developer workflows, giving security teams granular control over where, when, and how different findings are presented to developers (IDE, PR comment, etc.)

The Semgrep AppSec Platform works out-of-the-box with 20000+ proprietary rules across SAST, SCA, and secrets. Pro rules are written and maintained by the Semgrep security research team and are highly accurate, meaning AppSec teams can feel confident bringing findings directly to developers without slowing them down.

Semgrep analyzes code locally on your computer or in your build environment: **by default, code is never uploaded**. [Get started →.](#getting-started-)

<a href="#option-1-getting-started-from-the-cli">
<img src="https://raw.githubusercontent.com/semgrep/semgrep/develop/images/semgrep-scan-cli.jpg" alt="Semgrep CLI image"/></a>

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

</a>
  <a href="https://go.semgrep.dev/slack">
    <img src="https://img.shields.io/badge/slack-3.5k%20members-green?style=flat-square" alt="Join Semgrep community Slack" />
  </a>
  <a href="https://github.com/semgrep/semgrep/issues/new/choose">
    <img src="https://img.shields.io/badge/issues-welcome-green?style=flat-square" alt="Issues welcome!" />
  </a>
  <a href="https://github.com/semgrep/semgrep#readme">
    <img src="https://img.shields.io/github/stars/semgrep/semgrep?label=GitHub%20Stars&style=flat-square" alt="Star Semgrep on GitHub" />
  </a>
  <a href="https://hub.docker.com/r/semgrep/semgrep">
    <img src="https://img.shields.io/docker/pulls/semgrep/semgrep.svg?style=flat-square" alt="Docker Pulls" />
  </a>
  <a href="https://hub.docker.com/r/semgrep/semgrep">
    <img src="https://img.shields.io/docker/pulls/semgrep/semgrep.svg?style=flat-square" alt="Docker Pulls (Old)" />
  </a>
  <a href="https://twitter.com/intent/follow?screen_name=semgrep">
    <img src="https://img.shields.io/twitter/follow/semgrep?label=Follow%20semgrep&style=social&color=blue" alt="Follow @semgrep on Twitter" />
  </a>
</p>
</br>

Semgrep is a fast, open-source, static analysis tool that searches code, finds bugs, and enforces secure guardrails and coding standards. Semgrep [supports 30+ languages](#language-support) and can run in an IDE, as a pre-commit check, and as part of CI/CD workflows.

Semgrep is semantic grep for code. While running `grep "2"` would only match the exact string _2_, Semgrep would [match `x = 1; y = x + 1` when searching for _2_](https://semgrep.dev/playground/s/5rKgj). Semgrep rules look like the code you already write; no abstract syntax trees, regex wrestling, or painful DSLs.

Note that in security contexts, Semgrep Community Edition will miss many true positives as it can only analyze code within the boundaries of a single function or file. If you want to use Semgrep for security purposes (**SAST**, **SCA**, or **secrets scanning**), the Semgrep AppSec Platform is strongly recommended since it adds the following critical capabilities:

1. Improved core analysis capabilities (cross-file, cross-function, data-flow reachability) that greatly reduce false positives by 25% and increase detected true positives by 250%
2. Contextual post-processing of findings with Semgrep Assistant (AI) to further reduce noise by [~20%](https://a.storyblok.com/f/151984/x/2d12dc0223/whitepaper_-ai-powered-appsec-engineer-automate.pdf?cv=1728584410408).  In addition, Assistant enriches findings with tailored, step-by-step remediation guidance that humans find actionable >80% of the time.
3. Customizable policies and seamless integration into developer workflows, giving security teams granular control over where, when, and how different findings are presented to developers (IDE, PR comment, etc.)

The Semgrep AppSec Platform works out-of-the-box with 20000+ proprietary rules across SAST, SCA, and secrets. Pro rules are written and maintained by the Semgrep security research team and are highly accurate, meaning AppSec teams can feel confident bringing findings directly to developers without slowing them down.

Semgrep analyzes code locally on your computer or in your build environment: **by default, code is never uploaded**. [Get started →.](#getting-started-)

<a href="#option-1-getting-started-from-the-cli">
<img src="https://raw.githubusercontent.com/semgrep/semgrep/develop/images/semgrep-scan-cli.jpg" alt="Semgrep CLI image"/></a>

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | C/C++ / Make |
| Manifests detected | Makefile |
| Files in snapshot | 552 |
| Lines of code | 52010 |
| Dependency references | 17 |
| Dependencies by ecosystem | pypi: 17 |
| Upstream license | LGPL-2.1 |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| pypi | attrs | >=21.3 | cli/pyproject.toml |
| pypi | boltons | ~=21.0 | cli/pyproject.toml |
| pypi | click-option-group | ~=0.5 | cli/pyproject.toml |
| pypi | click | ~=8.4.2 | cli/pyproject.toml |
| pypi | colorama | ~=0.4.0 | cli/pyproject.toml |
| pypi | exceptiongroup | ~=1.2.0 | cli/pyproject.toml |
| pypi | glom | >=23.3 | cli/pyproject.toml |
| pypi | jsonschema | ~=4.25.1 | cli/pyproject.toml |
| pypi | mcp | ==1.29.0 | cli/pyproject.toml |
| pypi | opentelemetry-api | ~=1.37.0 | cli/pyproject.toml |
| pypi | opentelemetry-sdk | ~=1.37.0 | cli/pyproject.toml |
| pypi | opentelemetry-exporter-otlp-proto-http | ~=1.37.0 | cli/pyproject.toml |
| pypi | opentelemetry-instrumentation-requests | ~=0.58b0 | cli/pyproject.toml |
| pypi | opentelemetry-instrumentation-threading | ~=0.58b0 | cli/pyproject.toml |
| pypi | packaging | >=21.0 | cli/pyproject.toml |
| ... | (2 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

<a href="#option-1-getting-started-from-the-cli">
<img src="https://raw.githubusercontent.com/semgrep/semgrep/develop/images/semgrep-scan-cli.jpg" alt="Semgrep CLI image"/></a>

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `CONTRIBUTING.md`:*

<!--
   Unfortunately GitHub doesn't render symlinks as clickable, otherwise
   this file would be a symlink.
-->

Thank you for your interest in contributing to the Semgrep source code!

Find contribution guidelines in **[Semgrep documentation](https://semgrep.dev/docs/contributing/contributing/)**.

Specifically, see **[Contributing code](https://semgrep.dev/docs/contributing/contributing-code/)** to contribute either to Semgrep source code or semgrep-core source code.

## Quick start
Here's a quick way to get Semgrep building from source. See the documentation referenced above for detailed instructions

### Install prerequisites
The following dependencies need to be installed:
* [uv](https://docs.astral.sh/uv/getting-started/installation/)
* [bash](https://www.gnu.org/software/bash/)
* [opam](https://opam.ocaml.org/)

To install these on MacOS, run `make configure-osx`. Otherwise install these dependencies through the appropriate package manager, and then run `make configure`.

Now we can setup the OCaml dependencies, and install Semgrep:

```sh
# Install OCaml dependencies
make setup
# Build the OCaml binaries under `bin/`
make
# install the CLI wrapper in `cli/` in editable mode
# w/freshly built OCaml binary included
make install
# run tests
make test
```

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: LGPL-2.1** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
                  GNU LESSER GENERAL PUBLIC LICENSE
                       Version 2.1, February 1999

 Copyright (C) 1991, 1999 Free Software Foundation, Inc.
 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301  USA
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

[This is the first released version of the Lesser GPL.  It also counts
 as the successor of the GNU Library Public License, version 2, hence
 the version number 2.1.]

                            Preamble

  The licenses for most software are designed to take away your
freedom to share and change it.  By contrast, the GNU General Public
Licenses are intended to guarantee your freedom to share and change
free software--to make sure the software is free for all its users.

  This license, the Lesser General Public License, applies to some
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original LGPL-2.1 terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `LGPL-2.1` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `SEMGREP_PRIOR_DOCS` (category: SOFTWARE DEVELOPMENT)
- **Upstream URL:** https://github.com/semgrep/semgrep
- **Pinned commit (SHA):** `31729a1719c6e76ac8d41ec8fb9ab191621ee10f`
- **Branch:** develop
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`e4f0f80ea116bba4c6074b70d21d4344d80dff2d2edb7c8e21eb5381f731ef3d`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| DANS (KNAW/NWO, Netherlands) | 10.17026/PT | EU-recognised archive |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe
and Mail, Business Insider, National Post, Financial Post, StreetInsider,
Digital Journal, Barchart, International Business Times, and Fox News.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

