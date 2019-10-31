FROM docker.elastic.co/kibana/kibana:6.8.3
USER ROOT
ADD kibana.yml /usr/share/kibana/config/
RUN chown kibana:kibana /usr/share/kibana/config/kibana.yml
