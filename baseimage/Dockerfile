#Guru Project
#Docker Base Image

FROM ubuntu:14.04
MAINTAINER Tony Ayres <tony.ayres@dcu.ie>

RUN apt-get update
RUN apt-get -q -y install openssl 
RUN apt-get -q -y install wget

RUN wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u45-b14/jdk-8u45-linux-x64.tar.gz -o /jdk-8u45-linux-x64.tar.gz

RUN wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/7u79-b15/jdk-7u79-linux-x64.tar.gz -o /jdk-7u79-linux-x64.tar.gz

RUN mkdir /usr/lib/jdk 

RUN tar xvf /jdk-7u79-linux-x64.tar.gz -C /usr/lib/jdk
RUN tar xvf /jdk-8u45-linux-x64.tar.gz -C /usr/lib/jdk

RUN rm /jdk-7u79-linux-x64.tar.gz && rm /jdk-8u45-linux-x64.tar.gz

ENV PATH=$PATH:/usr/lib/jdk/jdk1.7.0_79/bin

CMD []

