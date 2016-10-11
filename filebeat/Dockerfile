FROM busybox:latest

RUN wget http://download.elastic.co/beats/filebeat/filebeat-1.3.1-x86_64.rpm
RUN rpm -i filebeat-1.3.1-x86_64.rpm
COPY ./config/filebeat.yml /etc/filebeat/filebeat.yml

ENTRYPOINT ["/etc/init.d/filebeat", "start"]