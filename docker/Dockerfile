FROM openjdk:8u322-jdk-bullseye

ARG MAVEN_VERSION=3.6.3

RUN mkdir -p /opt && \
    cd /opt && \
    curl -LO https://dlcdn.apache.org/maven/maven-3/$MAVEN_VERSION/binaries/apache-maven-$MAVEN_VERSION-bin.tar.gz && \
    tar -xvzf apache-maven-$MAVEN_VERSION-bin.tar.gz && \
    rm apache-maven-$MAVEN_VERSION-bin.tar.gz

ENV PATH $PATH:/opt/apache-maven-$MAVEN_VERSION/bin

RUN useradd -ms /bin/bash kafka
