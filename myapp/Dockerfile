FROM docker.elastic.co/elasticsearch/elasticsearch:6.8.3
USER root
RUN mkdir -p /var/log/elasticsearch /var/log/elasticsearch /var/lib/elasticsearch /opt/elasticsearch/data
RUN chown -R elasticsearch:elasticsearch /var/log/elasticsearch /var/log/elasticsearch /var/lib/elasticsearch /opt/elasticsearch
ADD elasticsearch.yml /usr/share/elasticsearch/config/
RUN chown elasticsearch:elasticsearch config/elasticsearch.yml
USER elasticsearch
WORKDIR /usr/share/elasticsearch
RUN bin/elasticsearch-plugin install -b discovery-ec2
