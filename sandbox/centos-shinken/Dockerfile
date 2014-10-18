# Dockerfile deploying jmeter ready to go
FROM maxholman/centos7

RUN yum install -y epel-release && yum install -y python-pip python-pycurl
RUN groupadd shinken && useradd shinken -g shinken && pip install shinken

