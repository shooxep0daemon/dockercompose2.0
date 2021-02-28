FROM maven:ibmjava-alpine
RUN apk update && apk add git
ENV CATALINA_HOME /usr/local/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH
RUN mkdir -p "$CATALINA_HOME"
WORKDIR $CATALINA_HOME
RUN wget https://downloads.apache.org/tomcat/tomcat-9/v9.0.43/bin/apache-tomcat-9.0.43.tar.gz -O /tmp/tomcat.tar.gz
RUN cd /tmp && tar xvfz tomcat.tar.gz
RUN cp -Rv /tmp/apache-tomcat-9.0.43/* /usr/local/tomcat/
WORKDIR /app
RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git
WORKDIR ./App42PaaS-Java-MySQL-Sample
RUN mvn clean
RUN mvn install
WORKDIR ./target
RUN cp App42PaaS-Java-MySQL-Sample-0.0.1-SNAPSHOT.war $CATALINA_HOME/webapps
WORKDIR $CATALINA_HOME
EXPOSE 8080
CMD ["catalina.sh", "run"]