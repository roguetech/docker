FROM docker.elastic.co/elasticsearch/elasticsearch:6.8.3
USER root
RUN mkdir -p /var/log/elasticsearch /var/log/elasticsearch /var/lib/elasticsearch
RUN chown -R elasticsearch:elasticsearch /var/log/elasticsearch /var/log/elasticsearch /var/lib/elasticsearch
ADD elasticsearch.yml /usr/share/elasticsearch/config/
RUN chown elasticsearch:elasticsearch config/elasticsearch.yml
RUN usermod -aG root elasticsearch
USER elasticsearch
WORKDIR /usr/share/elasticsearch
RUN mkdir -p /usr/share/elasticsearch/data
RUN bin/elasticsearch-plugin install -b discovery-ec2
