FROM ubuntu:20.04

RUN apt update && apt install -y openjdk-8-jdk wget ssh rsync

# Cài đặt Hadoop
RUN wget https://archive.apache.org/dist/hadoop/common/hadoop-3.3.6/hadoop-3.3.6.tar.gz && \
    tar -xzf hadoop-3.3.6.tar.gz && mv hadoop-3.3.6 /usr/local/hadoop

ENV HADOOP_HOME=/usr/local/hadoop
ENV PATH=$HADOOP_HOME/bin:$HADOOP_HOME/sbin:$PATH

COPY core-site.xml /usr/local/hadoop/etc/hadoop/
COPY hdfs-site.xml /usr/local/hadoop/etc/hadoop/

CMD ["hdfs", "namenode", "-format"]
