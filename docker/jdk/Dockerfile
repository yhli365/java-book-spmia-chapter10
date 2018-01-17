############################################################
# Dockerfile: [Spring Microservices in Action] Base Image
# docker build -t yhli365/tmx-jdk:1.0 .
# Usage:
#   - FROM yhli365/tmx-jdk:1.0
############################################################

FROM openjdk:8u151-jdk-alpine
#FROM openjdk:8-jdk-alpine

RUN apk update && apk upgrade && apk add netcat-openbsd && apk add curl

#@Features:jce_policy
RUN echo $JAVA_HOME
RUN cd /tmp/ && \
    curl -k -LO "http://download.oracle.com/otn-pub/java/jce/8/jce_policy-8.zip" -H 'Cookie: oraclelicense=accept-securebackup-cookie' && \
    unzip jce_policy-8.zip && \
    rm jce_policy-8.zip && \
    yes |cp -v /tmp/UnlimitedJCEPolicyJDK8/*.jar /usr/lib/jvm/java-1.8-openjdk/jre/lib/security/
