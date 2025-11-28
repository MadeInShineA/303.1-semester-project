# 303.1-semester-project

This repo contains the content of my semester project done in the 303.1 - Semester project course

## Gantt diagram (see [link](https://view.monday.com/5088330065-1288816531bffa22bf4ce0c331682f87?r=euc1))

![Gantt diagram image](./src/gantt.png)

## TODO

- [ x ] Create a barebones report with a gantt diagram
- [ ] Start working on the presentation
  - [ ] Impact slide
- [ ] Do the exclusion predict test
- [ x ] Understand the predict function better and why it seems to behave strangely regarding scale

## Daily diary

### 24.11.2025

- Made a [pull request](https://github.com/nipreps/nipreps-book/pull/49) to the [Nipreps book repo](https://github.com/nipreps/nipreps-book)
- Realised the different DIPY tutorials
- Started reading the Nipreps book

### 25.11.2025

- Meeting with Prof. Esteban
- Prepared the DIPY development environment
  - Installation steps
    - Create a venv and source it (or use uv venv and uv pip ...)
    - To build the project
      - sudo dnf install python3-devel
      - pip install -r requirements/build.txt
      - pip install --no-build-isolation -e .
    - To build the documentation
      - pip install sphinx
      - pip install sphinx_gallery
      - pip install numpydoc
      - pip install sphinxcontrib-bibtex
      - pip install sphinx-design
      - pip install grg-sphinx-theme
    - To use the correct formatting
      - pip install --no-build-isolation -e .\[style\]
      - pip install pre-commit
      - pre-commit install
- Started to look at the current gqi predict code and pull request
- Continued reading the Nipreps book (tried to fix a latex rendering error unsuccessfully)

### 26.11.2025

- Finished reading the Nipreps book
- Continued to look at the current gqi code and made small changes on the [enh/gqi-predict-dev](https://github.com/MadeInShineA/dipy/tree/enh/gqi-predict-dev) branch
  - Changed GeneralizedQSamplingFit odf function to take a sphere parameter (see [commit](https://github.com/MadeInShineA/dipy/commit/d9ab2bd51ae442b6c106244315a8090af6ce30c4))
  - Changed the GeneralizedQSamplingFit predict function to use clamping to remove negative value predictions (see [commit](https://github.com/MadeInShineA/dipy/commit/2ff80c8add7eb7896eac8b948e2f052ac91e150d))
- Created a small [marimo](https://marimo.io/) notebook to test and understand the prediction function on the [enh/gqi-predict-notebooks](https://github.com/MadeInShineA/dipy/tree/enh/gqi-predict-notebooks) branch (see [commit](https://github.com/MadeInShineA/dipy/commit/b88191ede9cbf39a9bcd0e35c0440921034135b7))

### 27.11.2025

- Changed the GeneralizedQSamplingFit predict function to use the model mode when calling the predict_kernel function. Also made the predict function work for multi-voxels (see [commit](https://github.com/MadeInShineA/dipy/commit/f4e7f9b35e8efef03293bb86f40649bea517fc01))
- Started gqi predict tests with (see [commit](https://github.com/MadeInShineA/dipy/commit/f4e7f9b35e8efef03293bb86f40649bea517fc01))
  - Single-voxel basic test
  - Single-voxel meaningful test
  - Multi-voxel basic test
  - Multi-voxel meaningful test
- Meeting with Prof. Esteban
- Did 2 marimo notebooks on the [enh/gqi-predict-notebooks](https://github.com/MadeInShineA/dipy/tree/enh/gqi-predict-notebooks) branch (see [commit](https://github.com/MadeInShineA/dipy/commit/0ad9d65fb0a7e4a5973afa21005b2080a60055cb))
  - A notebook regarding the roundtrip predictions on already seen data (see [notebook](https://olivier.amacker.dev/303.1-semester-project/dipy/gqi_roundtrip_notebook.html))
  - A notebook regarding cross voxel predictions (see [notebook](https://olivier.amacker.dev/303.1-semester-project/dipy/gqi_cross_voxel_notebook.html))
- Created the 303.1-semester-project github page (see [page](https://olivier.amacker.dev/303.1-semester-project/))

### 28.11.2025

- Create the Gantt diagram

## Sources

- DIPY
  - [DIPY website](https://dipy.org/)
  - [DIPY contributing guide](https://github.com/dipy/dipy/blob/master/.github/CONTRIBUTING.md)
  - [DIPY developer guide](https://docs.dipy.org/stable/devel/intro.html)
  - Tutorials
    - [Reconstruct with Constant Solid Angle (Q-Ball)](https://docs.dipy.org/stable/examples_built/reconstruction/reconst_csa.html)
    - [Reconstruct with Generalized Q-Sampling Imaging](https://docs.dipy.org/stable/examples_built/reconstruction/reconst_gqi.html)
    - [Introduction to Basic Tracking](https://docs.dipy.org/stable/examples_built/fiber_tracking/tracking_introduction_eudx_1.html)

- Youtube videos
  - [Diffusion Weighted Imaging - Doctor Klioze](https://www.youtube.com/watch?v=J_aamnpRJE8&list=LL&index=2)
  - [Diffusion Tensor Imaging (DTI) - Doctor Klioze](https://www.youtube.com/watch?v=twsV81UFFcE)
  - [Diffusion Tensor Imaging (DTI) Explained! | Neuroscience Methods 101 - Psyched!](https://www.youtube.com/watch?v=Be51OqnBbdc)
  - [DWI vs ADC MRI sequences: EXPLAINED - Radiology Tutorials](https://www.youtube.com/watch?v=GwCRBQt2WdM)

- Other
  - [Nipreps book](https://github.com/nipreps/nipreps-book)
  - [Prof. Esteban DIPY pull request](https://github.com/dipy/dipy/pull/3553)
  - [Prof. Esteban DIPY fork](https://github.com/oesteban/dipy/tree/enh/gqi-predict)
  - [Marimo website](https://marimo.io/)
