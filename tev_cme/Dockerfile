# syntax=docker/dockerfile:1

FROM ubuntu
RUN apt update
RUN apt install python3 -y
COPY cme /usr/local/bin/cme
COPY cmedb /usr/local/bin/cmedb
RUN chmod +x /usr/local/bin/cme
RUN chmod +x /usr/local/bin/cmedb
ENTRYPOINT [ "/usr/local/bin/cme" ]