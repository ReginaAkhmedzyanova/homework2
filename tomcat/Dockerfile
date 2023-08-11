FROM tomcat:8.0.51-jre8-alpine
WORKDIR /data
ADD hello-1.0/* /usr/local/tomcat/webapps/

EXPOSE 8080

CMD ["catalina.sh", "run"]