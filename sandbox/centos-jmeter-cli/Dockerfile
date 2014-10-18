# Dockerfile deploying jmeter ready to go
FROM maxholman/centos7

RUN yum install -y java-1.7.0-openjdk-headless wget vim
RUN wget http://mirror.bbln.org/apache/jmeter/binaries/apache-jmeter-2.11.tgz -O - | tar -C /opt/ -xzf -

