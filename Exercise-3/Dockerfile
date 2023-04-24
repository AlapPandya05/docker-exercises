FROM ubuntu:22.04
LABEL author="Alap Pandya"
ENV PING_TARGET "google.com"
RUN apt-get update
RUN apt-get update \
    && apt-get install -y iputils-ping \
    && apt-get clean \
    && cd /var/lib/apt/lists && rm -fr *Release* *Sources* *Packages* \
    && truncate -s 0 /var/log/*log
RUN apt-get install -y iputils-ping
CMD ["bash","-c", "ping $PING_TARGET"]
