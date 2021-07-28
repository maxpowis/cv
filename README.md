![repo size](https://img.shields.io/github/repo-size/maxpowis/cv)
![license](https://img.shields.io/github/license/maxpowis/cv)
![last commit](https://img.shields.io/github/last-commit/maxpowis/cv)

Contains the LaTeX source for my CV.

You can find me on [![Twitter][1.2]][1], or on [![LinkedIn][3.2]][3].

## Features

The source code was forked and adapted from [Professional CV](https://github.com/hmemcpy/cv) by Igal Tabachnik.

Peronal add-ons:

* Github actions for build & release
* helpers for employer & job records
* compute age and experience durations
* Github relaese version embedded in the pdf

## Preview

Page 1 | Page 2 | Page 3
:--------------:|:---------------:|:---------------:
![cv1](https://max.pow.is/assets/img/cv/cv-00.png)| ![cv2](https://max.pow.is/assets/img/cv/cv-01.png)| ![cv3](https://max.pow.is/assets/img/cv/cv-02.png)

## Developing

### Built With
Build with lualatex due to some known issues with FontAwesome.

### Prerequisites
Lualatex can be installed easily as part of [TexLive](https://www.tug.org/texlive/quickinstall.html)

### Setting up Dev

I personally use VSCode with a WSL2-debian for development and testing tasks.

Setup the debian WSL2 instance as follows:

```shell
sudo apt install git texlive texlive-luatex texlive-fonts-extra
```

The open the cloned project in the WSL2-debian context

### Building

Building is just a matter of clicking the build button in VSCode in this setup.

Note the github project comme with some release managemnt workflows:
* build.yml: builds the cv.tex project with lualatex
* release.yml: build and release to the repo releases
* deploy.yml: copies the latest pdf release to a github pages site repo.
* png.yml: generates thumbnails to be embedded in this README

<!-- Icons -->

[1.2]: http://i.imgur.com/wWzX9uB.png (twitter icon without padding)
[2.2]: https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/linkedin-3-16.png (LinkedIn icon without padding)

<!-- Links to your social media accounts -->

[1]: https://twitter.com/maxpowis
[2]: https://be.linkedin.com/in/maxpowis