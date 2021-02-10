#FROM alpine
#FROM openjdk:8-jre-alpine
FROM maven:ibmjava-alpine
#trying other image with alpine and jdk
RUN apk update && apk add git
WORKDIR /app
RUN git clone https://github.com/shooxep0daemon/testrepo.git
WORKDIR ./testrepo/app/
RUN mvn package
WORKDIR ./target/
RUN cp  hello-world-1.0-SNAPSHOT.jar /appdata
#package so libraries r adde 2 run from bash
