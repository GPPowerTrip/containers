FROM gliderlabs/alpine:3.3

RUN apk add --no-cache python3 && \
    apk add --no-cache --virtual=build-dependencies wget ca-certificates && \
    wget "https://bootstrap.pypa.io/get-pip.py" -O /dev/stdout | python3 && \
    apk del build-dependencies && \
    pip3 install requests

WORKDIR /root

ADD excalibot /usr/sbin/excalibot

ENV AHOST arthur
ENV APORT 8080

CMD excalibot
