FROM ubuntu
COPY o365creeper.py ./
RUN apt-get update && apt-get -y install python2
ENTRYPOINT ["python2.7" "o365creeper.py"]
CMD []