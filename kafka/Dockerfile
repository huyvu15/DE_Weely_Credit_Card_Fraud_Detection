FROM ubuntu:20.04

RUN apt update && apt install -y openjdk-8-jdk wget

# Cài đặt Kafka
RUN wget https://archive.apache.org/dist/kafka/3.5.1/kafka_2.13-3.5.1.tgz && \
    tar -xzf kafka_2.13-3.5.1.tgz && mv kafka_2.13-3.5.1 /usr/local/kafka


ENV KAFKA_HOME=/usr/local/kafka
ENV PATH=$KAFKA_HOME/bin:$PATH

CMD ["kafka-server-start.sh", "/usr/local/kafka/config/server.properties"]
