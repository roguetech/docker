FROM docker.elastic.co/elasticsearch/elasticsearch:6.8.3
USER root
RUN mkdir -p /var/log/elasticsearch
RUN mkdir -p /var/log/elasticsearch
RUN mkdir -p /var/lib/elasticsearch
RUN chown elasticsearch:elasticsearch /var/log/elasticsearch /var/log/elasticsearch /var/lib/elasticsearch
ADD elasticsearch.yml /usr/share/elasticsearch/config/
RUN chown elasticsearch:elasticsearch config/elasticsearch.yml
USER elasticsearch
WORKDIR /usr/share/elasticsearch
RUN bin/elasticsearch-plugin install -b discovery-ec2
