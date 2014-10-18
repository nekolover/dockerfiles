# Dockerfile building a doozerd container for testing
FROM centos:latest

RUN yum install -y tar iproute
RUN curl -L https://github.com/downloads/ha/doozerd/doozerd-0.8-linux-amd64.tar.gz -o /tmp/doozerd.tgz && cd /usr/local/bin && tar --wildcards --strip-components=1 -xf /tmp/doozerd.tgz 'doozerd*/doozerd' && rm -f /tmp/doozerd.tgz
RUN curl -L https://github.com/downloads/ha/doozer/doozer-0.8-linux-amd64.tar.gz -o /tmp/doozer.tgz && cd /usr/local/bin && tar --wildcards --strip-components=1 -xf /tmp/doozer.tgz 'doozer*/doozer' && rm -f /tmp/doozer.tgz

CMD /usr/local/bin/doozerd -timeout 5 -l $(ip route get 8.8.8.8 | head -1 | cut -d' ' -f8):8046

