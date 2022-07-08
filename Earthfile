VERSION 0.6
FROM earthly/dind:alpine

deps:
    FROM ubuntu

    RUN apt-get update
    RUN apt-get upgrade -y
    RUN apt-get install -y curl unzip
    
    RUN curl https://bun.sh/install | bash

    ENV BUNPATH /root/.bun
    ENV PATH $BUNPATH/bin:$PATH

    ENV BUN_VERSION = $(eval bun -v)    
    
    RUN mkdir /root/bun
    WORKDIR /root/bun

build:
    FROM +deps
    SAVE IMAGE --push oddiesea/bun:latest