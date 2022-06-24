FROM ubuntu

MAINTAINER apasoft.training@gmail.com

RUN mkdir /opt/tomcat/

WORKDIR /opt/tomcat
RUN apt -y update
RUN apt -y install curl
RUN curl -O https://apache.rediris.es/tomcat/tomcat-8/v8.5.76/bin/apache-tomcat-8.5.76.tar.gz
RUN tar xvfz apache*.tar.gz
RUN mv apache-tomcat-8.5.76/* /opt/tomcat/.
RUN apt -y install default-jdk
RUN java -version

WORKDIR /opt/tomcat/webapps
COPY app1.war .
EXPOSE 8080

