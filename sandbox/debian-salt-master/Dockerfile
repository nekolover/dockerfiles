# Dockerfile building a Debian Wheezy Salt Master for module testing
# Build it with docker build -t user/debian-salt-master . 
FROM debian:wheezy

RUN apt-get update && apt-get install -y wget
RUN wget -q -O- "http://debian.saltstack.com/debian-salt-team-joehealy.gpg.key" | apt-key add -
RUN echo "deb http://debian.saltstack.com/debian wheezy-saltstack main" > /etc/apt/sources.list.d/salt.list
RUN apt-get update
RUN apt-get install -y salt-master
RUN apt-get clean

