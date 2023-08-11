FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive 
ENV JAVA_HOME /usr/lib/jvm/java-11-openjdk-amd64

RUN apt update 
RUN apt install git wget default-jdk maven -y

WORKDIR /home/regina/homework2/app/
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello
WORKDIR /home/regina/homework2/app/boxfuse-sample-java-war-hello/
RUN mvn package 
CMD ["mvn"]
