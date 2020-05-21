# Download exporter binaries 
# @author: budongshu  
FROM alpine:3.9
MAINTAINER budongshu@haodf.com
#RUN apk --no-cache add wget
ENV NodeExporter=0.18.1
ENV MysqldExporter=0.12.1
ENV MongodbExporter=0.11.0
ENV Pgsql=0.8.0
#mysqld
RUN wget https://github.com/prometheus/mysqld_exporter/releases/download/v$MysqldExporter/mysqld_exporter-$MysqldExporter.linux-amd64.tar.gz && \
    mkdir -p /p8s && mv mysqld_exporter-$MysqldExporter.linux-amd64.tar.gz  /p8s/
#mongodb
RUN wget https://github.com/percona/mongodb_exporter/releases/download/v$MongodbExporter/mongodb_exporter-$MongodbExporter.linux-amd64.tar.gz && \
    mv /mongodb_exporter-$MongodbExporter.linux-amd64.tar.gz /p8s/
#node
RUN wget https://github.com/prometheus/node_exporter/releases/download/v$NodeExporter/node_exporter-$NodeExporter.linux-amd64.tar.gz && \ 
    mv node_exporter-$NodeExporter.linux-amd64.tar.gz /p8s/ 
#redis
RUN wget https://github.com/oliver006/redis_exporter/releases/download/v1.6.0/redis_exporter-v1.6.0.linux-amd64.tar.gz && \ 
    mv redis_exporter-v1.6.0.linux-amd64.tar.gz /p8s/
#rabbitmq
RUN wget https://github.com/rabbitmq/rabbitmq-prometheus/archive/v3.8.3.tar.gz  && \ 
    mv v3.8.3.tar.gz /p8s/  && \ 
    wget https://github.com/kbudde/rabbitmq_exporter/releases/download/v1.0.0-RC7/rabbitmq_exporter-1.0.0-RC7.linux-amd64.tar.gz && \ 
    mv rabbitmq_exporter-1.0.0-RC7.linux-amd64.tar.gz /p8s/  

CMD [ "sleep", "360000000" ]
