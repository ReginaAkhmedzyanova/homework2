FROM alpine:latest

ARG JAVA_HOME
ENV CATALINA_HOME /usr/local/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH
ENV DEBIAN_FRONTEND=noninteractive 

WORKDIR $CATALINA_HOME
RUN wget https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.78/bin/apache-tomcat-9.0.78.tar.gz && tar xvfz apache-tomcat-9.0.78.tar.gz
RUN cp -Rv ./apache-tomcat-9.0.78/* $CATALINA_HOME
RUN rm -rf apache-tomcat-9.0.78.tar.gz


EXPOSE 8080

CMD ["/usr/local/tomcat/bin/catalina.sh", "run"]