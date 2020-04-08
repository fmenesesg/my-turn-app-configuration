FROM alpine:latest

RUN apk --update add npm && \
    rm -rf /var/lib/apt/lists/* && \
    rm /var/cache/apk/*

VOLUME /src
WORKDIR /src
