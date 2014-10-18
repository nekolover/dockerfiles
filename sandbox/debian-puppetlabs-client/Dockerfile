# Dockerfile building a Debian Wheezy Puppet agent for module testing
FROM debian:wheezy

RUN apt-get update && apt-get install -y wget
RUN wget http://apt.puppetlabs.com/puppetlabs-release-wheezy.deb && dpkg -i puppetlabs-*deb && rm -f puppetlabs-*deb
RUN apt-get update
RUN apt-get install -y puppet hiera facter
RUN apt-get clean

