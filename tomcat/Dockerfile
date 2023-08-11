FROM alpine:latest

ENV TOMCAT_VERSION 9.0.78
ENV CATALINA_HOME /usr/local/tomcat
#ENV JAVA_HOME /usr/lib/jvm/java-11-openjdk-amd64
ENV PATH $CATALINA_HOME/bin:$PATH
ENV DEBIAN_FRONTEND=noninteractive 

#RUN apk update 
#RUN apk add default-jdk -y


WORKDIR $CATALINA_HOME
RUN apk update && wget https://archive.apache.org/dist/tomcat/tomcat-9/v${TOMCAT_VERSION}/bin/apache-tomcat-${TOMCAT_VERSION}.tar.gz -O ./tomcat.tar.gz
WORKDIR ./ && tar xvfz tomcat.tar.gz
RUN cp -Rv ./apache-tomcat-${TOMCAT_VERSION}/* $CATALINA_HOME
RUN rm -rf ./apache-tomcat-${TOMCAT_VERSION} && rm -rf ./tomcat.tar.gz


EXPOSE 8080

CMD ["/usr/local/tomcat/bin/catalina.sh", "run"]