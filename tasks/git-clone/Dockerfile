FROM alpine:latest

RUN apk --update add git less openssh && \
    rm -rf /var/lib/apt/lists/* && \
    rm /var/cache/apk/* && \
    mkdir -p /workspace /tekton/results && \
    chmod -R 755 /tekton /workspace

VOLUME /src
WORKDIR /src
