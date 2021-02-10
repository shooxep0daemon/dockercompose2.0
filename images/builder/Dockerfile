FROM maven:alpine
WORKDIR /app
COPY . /app
RUN mvn package
#package so libraries r adde 2 run from bash
CMD ["/bin/sh","sleep infinity"]