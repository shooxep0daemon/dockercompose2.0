#FROM alpine
#FROM openjdk:8-jre-alpine
FROM maven:ibmjava-alpine
#trying other image with alpine and jdk
RUN apk update && apk add git
WORKDIR /app
RUN git clone https://github.com/shooxep0daemon/testrepo.git
WORKDIR ./testrepo/app/
RUN mvn package
#package so libraries r added 2 run from bash
WORKDIR ./target/