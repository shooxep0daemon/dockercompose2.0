FROM maven:ibmjava-alpine
RUN apk update && apk add git
WORKDIR /app
RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git
WORKDIR ./App42PaaS-Java-MySQL-Sample
RUN mvn clean
RUN mvn install
RUN apk add tomcat9
WORKDIR ./target
RUN cp App42PaaS-Java-MySQL-Sample-0.0.1-SNAPSHOT.war $CATALINA_HOME/webapps
WORKDIR $CATALINA_HOME
EXPOSE 8080
CMD ["catalina.sh", "run"]