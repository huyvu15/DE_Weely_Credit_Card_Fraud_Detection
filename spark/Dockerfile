FROM ubuntu:20.04

RUN apt update && apt install -y openjdk-8-jdk wget python3 python3-pip

# Cài đặt Spark
RUN wget https://downloads.apache.org/spark/spark-3.2.1/spark-3.2.1-bin-hadoop3.2.tgz && \
    tar -xzf spark-3.2.1-bin-hadoop3.2.tgz && mv spark-3.2.1-bin-hadoop3.2 /usr/local/spark

ENV SPARK_HOME=/usr/local/spark
ENV PATH=$SPARK_HOME/bin:$PATH

CMD ["pyspark"]
