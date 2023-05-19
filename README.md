![repo size](https://img.shields.io/github/repo-size/maxpowis/cv)
![license](https://img.shields.io/github/license/maxpowis/cv)
![last commit](https://img.shields.io/github/last-commit/maxpowis/cv)

Contains the LaTeX source for my CV.

## Features

The source code was forked and adapted from [Professional CV](https://github.com/hmemcpy/cv) by Igal Tabachnik.

Peronal add-ons:

* compute age
* helpers for employer & job records with computed experience durations
* GitHub actions
  * build & release with version numbering embedded in the generated pdf
  * publish latest release to my  GitHub    static site repo
  * generate thumbnails (automatically pushed to my  GitHub   static site repo and embedded in this README)

## Preview

Page 1 | Page 2 | Page 3 | Page 4
:--------------:|:---------------:|:---------------:|:---------------:
![cv1](https://max.pow.is/assets/img/cv/cv-00.png)| ![cv2](https://max.pow.is/assets/img/cv/cv-01.png)| ![cv3](https://max.pow.is/assets/img/cv/cv-02.png)| ![cv4](https://max.pow.is/assets/img/cv/cv-03.png)

## Developing

### Built With
Build with lualatex due to some known issues with FontAwesome.

### Prerequisites

Lualatex can be installed easily as part of **[TexLive](https://www.tug.org/texlive/quickinstall.html)**

A package is also available for Windows but I prefer using a **WSL2** which is pretty well integrated with **VSCode**

### Setting up Dev

* *On debian*, the following packages must be installed
    ```shell
    sudo apt install git texlive texlive-luatex texlive-fonts-extra
    ```
* *On windows*, setup the debian instance as described above then open the cloned project in the WSL2 context
* *On MacOS*, the following packages must be installed
    ```shell
    brew install texlive
    ```

### Building

Touch a ´release.dat´ file locally to support embedding versioning of pdf file generation.

Building is just a matter of clicking the build button in VSCode in the VSCode setup.

Altrernatively, the pdf can be generated using the command-line:

```shell
# Generate the standard pdf
pdflatex cv
# Generate the pdf in dark mode
pdflatex "\def\darkmode{}\input{cv}"
```

Note the github project comes with some nice github actions:
* [![Build (Lualatex)](https://github.com/maxpowis/cv/actions/workflows/build.yml/badge.svg)](https://github.com/maxpowis/cv/actions/workflows/build.yml): builds the cv.tex project with lualatex
* [![Create Release](https://github.com/maxpowis/cv/actions/workflows/release.yml/badge.svg)](https://github.com/maxpowis/cv/actions/workflows/release.yml): build and release to the repo releases
* [![Publish PDF release to website](https://github.com/maxpowis/cv/actions/workflows/deploy.yml/badge.svg)](https://github.com/maxpowis/cv/actions/workflows/deploy.yml): copies the latest pdf release to a github pages site repo
* [![Convert PDF to PNG](https://github.com/maxpowis/cv/actions/workflows/png.yml/badge.svg)](https://github.com/maxpowis/cv/actions/workflows/png.yml): generates thumbnails to be embedded in this README
