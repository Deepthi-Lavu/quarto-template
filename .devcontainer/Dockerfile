FROM rocker/rstudio:latest

ENV PASSWORD=rstudio
ENV ROOT=TRUE

RUN apt-get update && apt-get install -y --no-install-recommends \
    wget \
    ca-certificates \
    gdebi-core \
    git \
    && rm -rf /var/lib/apt/lists/*

RUN wget https://github.com/quarto-dev/quarto-cli/releases/download/v1.8.24/quarto-1.8.24-linux-amd64.deb \
    && gdebi -n quarto-1.8.24-linux-amd64.deb \
    && rm quarto-1.8.24-linux-amd64.deb