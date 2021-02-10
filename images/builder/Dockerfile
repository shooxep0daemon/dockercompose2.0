FROM alpine
RUN apk update
RUN apk add maven
VOLUME /app /app
WORKDIR /app
RUN mvn package
#add libraries 2 run from bash
CMD ["/bin/sh","sleep infinity"]