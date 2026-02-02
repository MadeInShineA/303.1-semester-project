# 303.1-semester-project

[![Website olivier.amacker.dev/303.1-semester-project/index.html](https://img.shields.io/website-up-down-green-red/http/olivier.amacker.dev/303.1-semester-project/index.html.svg)](https://olivier.amacker.dev/303.1-semester-project/index.html)

This repo contains the content of my semester project done in the 303.1 - Semester project course

## Website

This project website is available [here](https://madeinshinea.github.io/303.1-semester-project/) or locally at `_site/index.html`

The website contains the following sections:

- [**Report**](https://madeinshinea.github.io/303.1-semester-project/src/report.html): Detailed documentation of the semester project
- [**Presentation**](https://madeinshinea.github.io/303.1-semester-project/src/presentation.html): Slides for the project presentation
- [**About me**](https://madeinshinea.github.io/303.1-semester-project/src/about_me): Slides presenting myself
- [**Daily Journal**](https://madeinshinea.github.io/303.1-semester-project/src/daily_journal.html): Chronological log of project progress and activities
- [**Sources**](https://madeinshinea.github.io/303.1-semester-project/src/sources.html): References and source materials used in the project

## Local Setup

To set up the project website locally:

1. Install [uv](https://docs.astral.sh/uv/getting-started/installation/)
2. Clone the repository
3. Run `uv sync` to install dependencies
4. Run `uv run quarto render` to build the site

The site will be in the `_site/` directory.

## Submodules

This repository uses Git submodules to include related projects:

- **dipy**: A personal fork of [Oesteban's DIPY fork](https://github.com/oesteban/dipy), which is itself a fork of the main [DIPY repository](https://github.com/dipy/dipy), incorporating improvements to the Generalized Q-Sampling Imaging (GQI) predict functionality originally implemented in [DIPY PR #3553](https://github.com/dipy/dipy/pull/3553) and further enhanced in [PR #1](https://github.com/oesteban/dipy/pull/1) of the Oesteban fork.
- **dipy-tutorial**: Educational notebooks and examples demonstrating the use of DIPY for diffusion MRI analysis.

- **nipreps-book**: A personal fork of the [NIPREPS book repository](https://github.com/nipreps/nipreps-book/tree/main), related to the external pull request ([PR #49](https://github.com/nipreps/nipreps-book/pull/49)) for updating the repository README.md links.

To initialize and update submodules after cloning:

```bash
git submodule init
git submodule update
```

## Related External Pull Requests

| PR | Status |
|----|--------|
| [DIPY PR #3553](https://github.com/dipy/dipy/pull/3553): ENH: Implement a predict() function for the GeneralizedQSamplingModel | ![PR status badge](https://img.shields.io/badge/status-open-blue.svg) |
| [Oesteban DIPY fork PR #1](https://github.com/oesteban/dipy/pull/1): Enhancements to GQI predict functionality | ![PR status badge](https://img.shields.io/badge/status-open-blue.svg) |
| [nipreps-book PR #49](https://github.com/nipreps/nipreps-book/pull/49): Update of README.md links (NiTransforms and Pixi) | ![PR status badge](https://img.shields.io/badge/status-merged-green.svg) |
