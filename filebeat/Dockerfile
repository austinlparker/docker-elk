FROM busybox:latest

RUN wget https://download.elastic.co/beats/filebeat/filebeat-1.3.1-x86_64.rpm
RUN sudo rpm -vi filebeat-1.3.1-x86_64.rpm
COPY ./config/filebeat.yml /etc/filebeat/filebeat.yml

ENTRYPOINT ["sudo", "/etc/init.d/filebeat", "start"]