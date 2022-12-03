# Containerized Tools

Installing tools like TeX Live might be hacky and tedious. Therefore, I create this repository, which contains Dockerfile(s) to create Docker images that have those tools installed within.

To use these images, you are gonna need Docker installed on your machine (obviously).

## TeX Live images

- Infraonly
  - [![Docker images for TeX Live](https://github.com/duong755/containerized-tools/actions/workflows/texlive-infraonly.yml/badge.svg)](https://github.com/duong755/containerized-tools/actions/workflows/texlive-infraonly.yml)
  - ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ngoquangduong/texlive/infraonly)
- Minimal
  - [![Docker images for TeX Live](https://github.com/duong755/containerized-tools/actions/workflows/texlive-minimal.yml/badge.svg)](https://github.com/duong755/containerized-tools/actions/workflows/texlive-minimal.yml)
  - ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ngoquangduong/texlive/minimal)
- Basic
  - [![Docker images for TeX Live](https://github.com/duong755/containerized-tools/actions/workflows/texlive-basic.yml/badge.svg)](https://github.com/duong755/containerized-tools/actions/workflows/texlive-basic.yml)
  - ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ngoquangduong/texlive/basic)
- Small
  - [![Docker images for TeX Live](https://github.com/duong755/containerized-tools/actions/workflows/texlive-small.yml/badge.svg)](https://github.com/duong755/containerized-tools/actions/workflows/texlive-small.yml)
  - ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ngoquangduong/texlive/small)
- ConTeXt
  - [![Docker images for TeX Live](https://github.com/duong755/containerized-tools/actions/workflows/texlive-context.yml/badge.svg)](https://github.com/duong755/containerized-tools/actions/workflows/texlive-context.yml)
  - ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ngoquangduong/texlive/context)
- GUST
  - [![Docker images for TeX Live](https://github.com/duong755/containerized-tools/actions/workflows/texlive-gust.yml/badge.svg)](https://github.com/duong755/containerized-tools/actions/workflows/texlive-gust.yml)
  - ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ngoquangduong/texlive/gust)
- Medium
  - [![Docker images for TeX Live](https://github.com/duong755/containerized-tools/actions/workflows/texlive-medium.yml/badge.svg)](https://github.com/duong755/containerized-tools/actions/workflows/texlive-medium.yml)
  - ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ngoquangduong/texlive/medium)
- teTeX
  - [![Docker images for TeX Live](https://github.com/duong755/containerized-tools/actions/workflows/texlive-tetex.yml/badge.svg)](https://github.com/duong755/containerized-tools/actions/workflows/texlive-tetex.yml)
  - ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ngoquangduong/texlive/tetex)
- Full
  - [![Docker images for TeX Live](https://github.com/duong755/containerized-tools/actions/workflows/texlive-scheme-full.yml/badge.svg)](https://github.com/duong755/containerized-tools/actions/workflows/texlive-scheme-full.yml)
  - ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/ngoquangduong/texlive/scheme-full)

### How to use

For example, you want to compile a `.tex` file with `pdflatex`, you can use:

```bash
docker run --rm --workdir /tmp --mount type=bind,src=$(pwd),target=/tmp ngoquangduong/texlive:scheme-full pdflatex main.tex
```

Warning: `TeX Live (scheme-full)` is extremely large.
