FROM alpine
RUN apk update
RUN apk add maven
VOLUME /app /app
WORKDIR /app
RUN mvn compile
CMD ["/bin/sh","sleep infinity"]