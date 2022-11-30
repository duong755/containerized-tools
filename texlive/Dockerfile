FROM alpine:3.16

ARG SCHEME=infraonly

RUN apk update && apk upgrade

RUN apk add --no-cache wget perl

RUN wget -qO /tmp/install-tl-unx.tar.gz http://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz

RUN mkdir -p /tmp/install-tl-latest && tar -xzf /tmp/install-tl-unx.tar.gz -C /tmp/install-tl-latest

COPY ./ /tmp/install-tl-latest

RUN cd /tmp/install-tl-latest/install-tl-* && \
    chmod +x ./install-tl && \
    ./install-tl --scheme=${SCHEME} --profile=/tmp/install-tl-latest/installation.profile

RUN rm -rf /tmp/install-tl-unx.tar.gz /tmp/install-tl-latest

ENV PATH="/usr/local/texlive/2022/bin/x86_64-linux:$PATH"

RUN tlmgr init-usertree
