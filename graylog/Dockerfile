FROM graylog/graylog:3.1

USER root

RUN apt-get update && apt-get install -y procps iproute2 telnet net-tools

ADD graylog.conf /usr/share/graylog/data/config/graylog.conf

RUN chown graylog:graylog /usr/share/graylog/data/config/graylog.conf
