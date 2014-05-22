# Dockerfile building a CentOS Puppet agent for module testing
FROM centos

RUN rpm -ivh http://mirrors.ircam.fr/pub/fedora/epel/6/i386/epel-release-6-8.noarch.rpm
RUN rpm -ivh http://yum.puppetlabs.com/puppetlabs-release-el-6.noarch.rpm
RUN yum makecache
RUN yum install -y puppet hiera facter

