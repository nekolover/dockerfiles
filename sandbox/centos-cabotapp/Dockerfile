# Dockerfile deploying cabot
FROM centos:latest

RUN yum install -y epel-release
RUN yum install -y git vim python-pip gcc g++ make python-dev build-essential redis-server libpq-dev rubygems libxml2-dev libxslt-dev nodejs npm postgresql-9.1 nginx htop
RUN mkdir -p /srv/apps/cabot && cd /srv/apps/cabot && git clone https://github.com/arachnys/cabot.git
RUN pip install -e /srv/apps/cabot/cabot --exists-action=w
RUN cd /srv/apps/cabot/cabot && foreman run python manage.py syncdb -e conf/production.env 



CMD /usr/local/bin/doozerd -timeout 5 -l $(ip route get 8.8.8.8 | head -1 | cut -d' ' -f8):8046

