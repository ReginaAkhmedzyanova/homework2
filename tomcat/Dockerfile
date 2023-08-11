FROM alpine:latest

ENV CATALINA_HOME /usr/local/tomcat
#ENV JAVA_HOME /usr/lib/jvm/java-11-openjdk-amd64
ENV PATH $CATALINA_HOME/bin:$PATH
ENV DEBIAN_FRONTEND=noninteractive 

#RUN apk update 
#RUN apk add default-jdk -y


WORKDIR $CATALINA_HOME
RUN apk update && wget https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.78/bin/apache-tomcat-9.0.78.tar.gz 
WORKDIR ./ && tar xvfz apache-tomcat-9.0.78.tar.gz
RUN cp -Rv ./apache-tomcat-9.0.78/* $CATALINA_HOME
RUN rm -rf ./apache-tomcat-9.0.78 && rm -rf ./apache-tomcat-9.0.78.tar.gz


EXPOSE 8080

CMD ["/usr/local/tomcat/bin/catalina.sh", "run"]