FROM postgres:9.4.3
MAINTAINER Wuxia <anguia@sina.com>

ENV DB_NAME aiwlanbi
ENV DB_USER aiwlanbi
ENV DB_PASS aiwlanbi

RUN mkdir /docker-entrypoint-initdb.d/config
ADD ./config /docker-entrypoint-initdb.d/config
ADD setupRemoteConnections.sh /docker-entrypoint-initdb.d/setupRemoteConnections.sh
RUN chmod 755 /docker-entrypoint-initdb.d/setupRemoteConnections.sh
ADD setup-database.sh /docker-entrypoint-initdb.d/setup-database.sh
RUN chmod 755 /docker-entrypoint-initdb.d/setup-database.sh
################################################################
#FROM ubuntu:14.04  
 
#MAINTAINER Wuxia <anguia@sina.com>  
  
#RUN apt-get update;   
  
#RUN apt-get install -y -q git python openssh-client

#ADD . /app
#WORKDIR /app

#RUN mkdir -p /root/.ssh/ 

#ADD ./config/id_rsa /root/.ssh/id_rsa
#ADD ./config/id_rsa /root/.ssh/id_rsa.pub

#RUN chmod 700 /root/.ssh/
#RUN chmod 600 /root/.ssh/id_rsa
#RUN chown -R root:root /root/.ssh

## Create known_hosts
#RUN touch /root/.ssh/known_hosts
#RUN echo "[clouddata.f3322.net]:10025,[183.48.73.240]:10025 ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDBnlaMRuoxrk3IzwUHRzP/rsXM6IDyDiV27byw3VZdaLwgxbQlKgTjrPxNse+jY8Eyvvonyb8+NahJaQc6e6gdA7kgDsk6bd1Ea9/dudilQgXvOW7SfsVGA1mfgW8oYiSlvXGVACpG7Mfpz45NK+6OQJxHAwHH+tP9yJFAvbC6jR3sab8TKDXs+28plAJJMcrDiWQP9VapLkb5zbv5YIe09QuNuxxb0OSZxnY/MXT76Rm36QymYmCKqhhDZn7zVWefqnTQQSD/DVa885ZLZkEntN0ShINu03PBcfqCP1LkDMES1zYD9MvDzBDGEkPgMxGoNlW/F9Qn0QMzIUFgtA4z" >/root/.ssh/known_hosts

#RUN cat /root/.ssh/id_rsa
#RUN ls /root/.ssh/
#RUN git clone ssh://git@clouddata.f3322.net:10025/cloud-data/webdemo.git 

#CMD python -m SimpleHTTPServer 5000
#EXPOSE 5000
