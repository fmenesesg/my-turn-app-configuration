FROM alpine:latest

RUN apk --update add npm && \
    rm -rf /var/lib/apt/lists/* && \
    rm /var/cache/apk/* && \
    mkdir -p /tekton/results && \
    chmod -R 755 /tekton

VOLUME /src
WORKDIR /src
