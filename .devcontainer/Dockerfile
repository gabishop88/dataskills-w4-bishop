FROM rocker/r-ver:latest

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        curl \
        ca-certificates \
        build-essential \
        libcurl4-openssl-dev \
        libssl-dev \
        libxml2-dev \
        libuv1-dev \
        libzmq3-dev \
        libglpk-dev \
    && rm -rf /var/lib/apt/lists/*

RUN groupadd vscode \
    && useradd --create-home --gid vscode vscode

COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/

ENV PATH="/home/vscode/.local/bin:/home/vscode/.venv/bin:$PATH"

RUN curl -fsSL https://quarto.org/download/latest/quarto-linux-amd64.deb \
    -o /tmp/quarto.deb \
    && apt-get update \
    && apt-get install -y /tmp/quarto.deb \
    && rm /tmp/quarto.deb \
    && rm -rf /var/lib/apt/lists/*
