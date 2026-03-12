FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

RUN apt-get update \
    && export DEBIAN_FRONTEND=noninteractive \
    && apt-get install -y --no-install-recommends \
        biber \
        latexmk \
        texlive-bibtex-extra \
        texlive-fonts-recommended \
        texlive-lang-german \
        texlive-latex-base \
        texlive-latex-extra \
        texlive-latex-recommended \
        texlive-pictures \
        texlive-science \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
