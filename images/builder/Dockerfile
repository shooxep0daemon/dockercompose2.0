FROM alpine
RUN apk update && apk add maven && apk add git
WORKDIR /app
RUN git clone https://github.com/shooxep0daemon/testrepo.git
WORKDIR /testrepo/app/
RUN mvn package
#package so libraries r adde 2 run from bash
CMD ["/bin/sh","sleep infinity"]