FROM ubuntu:20.04

RUN apt update && apt install -y openjdk-8-jdk wget

# Cài đặt HBase
RUN wget https://archive.apache.org/dist/hbase/2.4.15/hbase-2.4.15-bin.tar.gz && \
    tar -xzf hbase-2.4.15-bin.tar.gz && mv hbase-2.4.15 /usr/local/hbase

ENV HBASE_HOME=/usr/local/hbase
ENV PATH=$HBASE_HOME/bin:$PATH

COPY hbase-site.xml /usr/local/hbase/conf/

CMD ["start-hbase.sh"]
