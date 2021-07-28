![repo size](https://img.shields.io/github/repo-size/maxpowis/cv)
![license](https://img.shields.io/github/license/maxpowis/cv)
![last commit](https://img.shields.io/github/last-commit/maxpowis/cv)

Contains the LaTeX source for my CV.

You can find me on <img width="16px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" href= "https://be.linkedin.com/in/maxpowis"/>.

## Features

The source code was forked and adapted from [Professional CV](https://github.com/hmemcpy/cv) by Igal Tabachnik.

Peronal add-ons:

* Github actions for build & release
* Generate thumbnails for diplay in this readme
* helpers for employer & job records
* compute age and experience durations
* Github release version embedded in the pdf

## Preview

Page 1 | Page 2 | Page 3
:--------------:|:---------------:|:---------------:
![cv1](https://max.pow.is/assets/img/cv/cv-00.png)| ![cv2](https://max.pow.is/assets/img/cv/cv-01.png)| ![cv3](https://max.pow.is/assets/img/cv/cv-02.png)

## Developing

### Built With
Build with lualatex due to some known issues with FontAwesome.

### Prerequisites
Lualatex can be installed easily as part of **[TexLive](https://www.tug.org/texlive/quickinstall.html)**
A package is also available for Windows but I prefer using a **WSL2** which is pretty well integrated with **VSCode**

### Setting up Dev

*On debian*, the following packages must be installed

```shell
sudo apt install git texlive texlive-luatex texlive-fonts-extra
```

*On windows*, setup the debian instance as described above then open the cloned project in the WSL2 context

### Building

Building is just a matter of clicking the build button in VSCode in the VSCode setup.

Note the github project comes with some nice github actions:
* **build.yml**: builds the cv.tex project with lualatex
* **release.yml**: build and release to the repo releases
* **deploy.yml**: copies the latest pdf release to a github pages site repo
* **png.yml**: generates thumbnails to be embedded in this README
