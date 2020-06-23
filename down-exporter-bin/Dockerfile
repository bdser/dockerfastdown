# Download exporter binaries 
# @author: budongshu  
FROM alpine:3.9
MAINTAINER budongshu@haodf.com
#RUN apk --no-cache add wget
ENV NodeExporter=0.18.1
ENV MysqldExporter=0.12.1
ENV MongodbExporter=0.11.0
ENV Pgsql=0.8.0
RUN wget https://github.com/goharbor/harbor/releases/download/v1.10.3/harbor-offline-installer-v1.10.3.tgz && \
    mkdir -p /p8s && mv harbor-offline-installer-v1.10.3.tgz   /p8s/

CMD [ "sleep", "360000000" ]
