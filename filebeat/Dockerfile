FROM centos:latest

RUN curl -L -O https://download.elastic.co/beats/filebeat/filebeat-1.3.1-x86_64.rpm
RUN rpm -vi filebeat-1.3.1-x86_64.rpm
COPY ./config/filebeat.yml /etc/filebeat/filebeat.yml

ENTRYPOINT ["/etc/init.d/filebeat", "start"]