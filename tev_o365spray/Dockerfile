# syntax=docker/dockerfile:1

FROM alpine
COPY o365spray.py o365spray.py
COPY requirements.txt requirements.txt
COPY setup.py setup.py
COPY o365spray o365spray
RUN apk add build-base
ENV PYTHONUNBUFFERED=1
RUN apk add --update --no-cache python3 && ln -sf python3 /usr/bin/python
RUN python3 -m ensurepip
RUN pip3 install --no-cache --upgrade pip setuptools
RUN python3 -m pip install -r requirements.txt
RUN python3 -m pip install -r requirements.txt
ENTRYPOINT ["/usr/bin/python", "./o365spray.py" ]
CMD []