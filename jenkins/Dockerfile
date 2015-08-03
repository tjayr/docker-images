#Guru Project
#Docker container for Jenkins CI

FROM alpine:3.1
MAINTAINER Tony Ayres <tony.ayres@dcu.ie>

ENV JENKINS_HOME /opt/jenkins

#RUN apk add --update mysql-client && rm -rf /var/cache/apk/*

RUN wget http://mirrors.jenkins-ci.org/war/latest/jenkins.war -O /jenkins.war

RUN wget --no-check-certificate "https://github.com/grails/grails-core/releases/download/v2.4.3/grails-2.4.3.zip" -O /grails-2.4.3.zip

RUN mkdir -p /opt/grails
RUN mkdir -p /opt/jenkins

RUN unzip /grails-2.4.3.zip -d /opt/grails

RUN rm /grails-2.4.3.zip

EXPOSE 8080
ENTRYPOINT ["java", "-jar", "jenkins.war"]

