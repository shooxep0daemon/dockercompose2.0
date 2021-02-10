#FROM alpine
FROM openjdk:8-jre-alpine
#trying other image with alpine and jdk
RUN apk update && apk add maven && apk add git && apk add jdk
WORKDIR /app
RUN git clone https://github.com/shooxep0daemon/testrepo.git
WORKDIR ./testrepo/app/
RUN mvn package
#package so libraries r adde 2 run from bash
CMD ["/bin/sh","sleep infinity"]