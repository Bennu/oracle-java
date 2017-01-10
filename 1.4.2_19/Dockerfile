FROM ubuntu:16.10

ENV JAVA_HOME /usr/lib/jvm/j2sdk1.4.2_19
ENV PATH $PATH:$JAVA_HOME/jre/bin:$JAVA_HOME/bin

RUN apt-get update && apt-get install -y --no-install-recommends \
    wget \
    lib32z1 \
    lib32ncurses5 \
    ca-certificates && \
    wget --header "Cookie: oraclelicense=accept-securebackup-cookie;" \
         "http://download.oracle.com/otn-pub/java/j2sdk/1.4.2_19/j2sdk-1_4_2_19-linux-i586.bin" && \
    chmod 744 j2sdk-1_4_2_19-linux-i586.bin && yes | ./j2sdk-1_4_2_19-linux-i586.bin | grep yes && \
    rm j2sdk-1_4_2_19-linux-i586.bin && mkdir /usr/lib/jvm && mv j2sdk1.4.2_19 /usr/lib/jvm && \
    apt-get purge -y \
    wget \
    ca-certificates && \
    apt-get autoremove -y && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
