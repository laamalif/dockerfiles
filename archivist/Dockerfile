FROM alpine:edge
MAINTAINER Laam Alif <laamalif@pm.me>

RUN echo http://nl.alpinelinux.org/alpine/edge/testing >> /etc/apk/repositories
RUN apk --update add python3 py3-requests exiftool py3-beautifulsoup4 py3-lxml py3-pillow py3-img2pdf 
RUN rm -rf /var/cache/apk/*
RUN mkdir /rekhta
COPY rekhta /usr/bin/
WORKDIR /rekhta
ENTRYPOINT [ "rekhta" ]
