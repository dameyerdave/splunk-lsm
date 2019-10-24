FROM ubuntu:latest
MAINTAINER dameyerdave@gmail.com
RUN apt update
RUN apt install python3 python3-pip vim curl git -y
RUN mkdir -p /root/git; cd /root/git; git clone https://github.com/dameyerdave/lsmadmin
RUN mkdir -p /root/git/lsmadmin/lib; pip3 install pysqlite3 cherrypy ldap3 -t /root/git/lsmadmin/lib
EXPOSE 8080
WORKDIR /root
RUN python3 /root/git/lsmadmin/lsmadmin.py
