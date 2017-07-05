FROM debian:stretch

ENV JAVA_HOME /usr/lib/jvm/j2sdk1.4.2_19
ENV PATH $PATH:/usr/lib/jvm/j2sdk1.4.2_19/jre/bin:/usr/lib/jvm/j2sdk1.4.2_19/bin

RUN dpkg --add-architecture i386 && apt-get update && apt-get install -y --no-install-recommends \
    wget \
    lib32z1 \
    libc6:i386 \
    libxt6:i386 \
    libxtst6:i386 \
    libxext6:i386 \
    rm -rf /var/lib/apt/lists/* && \
    wget --header "Cookie: oraclelicense=accept-securebackup-cookie;" \
              "http://download.oracle.com/otn-pub/java/j2sdk/1.4.2_19/j2sdk-1_4_2_19-linux-i586.bin" && \
    chmod 744 j2sdk-1_4_2_19-linux-i586.bin && yes | ./j2sdk-1_4_2_19-linux-i586.bin | grep yes && \
    rm j2sdk-1_4_2_19-linux-i586.bin && mkdir /usr/lib/jvm && mv j2sdk1.4.2_19 /usr/lib/jvm

