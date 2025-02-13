FROM ubuntu:20.04

RUN apt update && apt install -y openjdk-8-jdk wget

# Cài đặt Sqoop
RUN wget https://archive.apache.org/dist/sqoop/1.4.7/sqoop-1.4.7.bin__hadoop-2.6.0.tar.gz && \
    tar -xzf sqoop-1.4.7.bin__hadoop-2.6.0.tar.gz && mv sqoop-1.4.7.bin__hadoop-2.6.0 /usr/local/sqoop

ENV SQOOP_HOME=/usr/local/sqoop
ENV PATH=$SQOOP_HOME/bin:$PATH

CMD ["bash"]
