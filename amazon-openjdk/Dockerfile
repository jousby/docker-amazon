FROM 137112412989.dkr.ecr.us-west-2.amazonaws.com/amazonlinux

# Default to UTF-8 file.encoding
ENV LANG C.UTF-8

ENV JAVA_HOME /usr/lib/jvm/java-1.8-openjdk
ENV PATH $PATH:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin

# Open a shell in an amazonlinux container to get the current available versions with:
# > docker run -ti amazonlinux bash
# > yum --showduplicates list java-1.8.0-openjdk-devel
ENV JAVA_VERSION 8u121
ENV JAVA_AMAZON_VERSION java-1.8.0-openjdk-devel-1.8.0.121-0.b13.29.amzn1

RUN set -x \
    && yum -y install which \
    && yum -y install $JAVA_AMAZON_VERSION
