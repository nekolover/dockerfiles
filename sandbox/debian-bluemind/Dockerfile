# Dockerfile building a Debian Wheezy Puppet agent for module testing
FROM debian:wheezy

RUN apt-get update && apt-get install -y wget
RUN echo "deb http://pkg.blue-mind.net/3.0.7/wheezy/main/ ./" > /etc/apt/sources.list.d/bm.list
RUN apt-get update
RUN apt-get install -y --force-yes bm-full bm-soap
RUN apt-get clean

