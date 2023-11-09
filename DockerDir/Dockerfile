FROM ubuntu:20.04

LABEL maintainer="alejandrogarcon@gmail.com"

#Java8
RUN apt-get update && apt-get install -y openjdk-8-jdk

#Tomcat8
RUN apt-get install -y tomcat8

#Jenkins
RUN mkdir -p /opt/jenkins
RUN curl -L https://updates.jenkins.io/latest/jenkins.war -o /opt/jenkins/jenkins.war

#Jenkins en Tomcat
COPY tomcat-users.xml /etc/tomcat8/tomcat-users.xml

# Puerto 8080
EXPOSE 8080

# Comando por defecto al iniciar el contenedor
CMD ["catalina.sh", "run"]
