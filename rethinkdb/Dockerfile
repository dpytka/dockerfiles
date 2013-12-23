FROM ubuntu:latest

RUN echo "deb http://archive.ubuntu.com/ubuntu precise main universe" > /etc/apt/sources.list

RUN apt-get update
RUN apt-get install -y python-software-properties
RUN add-apt-repository -y ppa:rethinkdb/ppa
RUN apt-get update 
apt-get -y upgrade

RUN apt-get -y install rethinkdb

EXPOSE 8080 28015 29015

CMD ["--bind", "all"]
ENTRYPOINT ["rethinkdb"]

