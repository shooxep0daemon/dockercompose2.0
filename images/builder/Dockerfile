FROM alpine
RUN apk update
RUN apk add maven
COPY ../home/newshoosha/apptest/testrepo/app /app
WORKDIR /app
RUN mvn package
#package so libraries r adde 2 run from bash
CMD ["/bin/sh","sleep infinity"]