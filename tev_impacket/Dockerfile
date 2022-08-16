# syntax=docker/dockerfile:1

FROM alpine
COPY impacket impacket
RUN apk add build-base
# RUN apk add --no-cache git
ENV PYTHONUNBUFFERED=1
RUN apk add --update --no-cache python3 && ln -sf python3 /usr/bin/python
RUN python3 -m ensurepip
RUN pip3 install --no-cache --upgrade pip setuptools
RUN python3 -m pip install -r ./impacket/requirements.txt
RUN python3 -m pip install ./impacket/.