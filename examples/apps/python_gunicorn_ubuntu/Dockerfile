FROM ubuntu:14.04

RUN apt-get update && \
		apt-get -y install python-software-properties python build-essential && \
		apt-get -y install python-dev && \
		apt-get -y install python-pip && \
		mkdir -p /opt/my/service

COPY service /opt/my/service

WORKDIR /opt/my/service

RUN pip install -r requirements.txt

EXPOSE 9000
ENTRYPOINT ["/opt/my/service/run.sh"]


