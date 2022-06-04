FROM ubuntu:20.04

ARG SCHEME=infraonly

RUN apt-get update -y && apt-get upgrade -y && apt-get install -y wget perl

RUN wget -qO /tmp/install-tl-unx.tar.gz http://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz

RUN mkdir -p /tmp/install-tl-latest && tar -xzf /tmp/install-tl-unx.tar.gz -C /tmp/install-tl-latest

COPY ./ /tmp/install-tl-latest

RUN cd /tmp/install-tl-latest/install-tl-* && \
    chmod +x ./install-tl && \
    ./install-tl --scheme=${SCHEME} --profile=/tmp/install-tl-latest/installation.profile

ENV PATH="/usr/local/texlive/2022/bin/x86_64-linux:$PATH"
