FROM ubuntu:16.10

ENV JAVA_HOME /usr/lib/jvm/jdk1.8.0_112
ENV PATH $PATH:$JAVA_HOME/jre/bin:$JAVA_HOME/bin

RUN apt-get update && apt-get install -y --no-install-recommends \
    wget \
    ca-certificates && \
    wget --header "Cookie: oraclelicense=accept-securebackup-cookie;" \
         "http://download.oracle.com/otn-pub/java/jdk/8u112-b15/jdk-8u112-linux-x64.tar.gz" && \
    tar zxvf jdk-8u112-linux-x64.tar.gz && rm jdk-8u112-linux-x64.tar.gz && \
    mkdir /usr/lib/jvm && mv jdk1.8.0_112 /usr/lib/jvm && \
    apt-get purge -y \
    wget \
    ca-certificates && \
    apt-get autoremove -y && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
