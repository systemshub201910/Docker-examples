FROM ubuntu

RUN apt-get update
RUN apt-get install -y apache2

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
RUN mkdir /etc/apache2/apache2-runtime
ENV APACHE_RUN_DIR  apache2-runtime
ENV APACHE_PID_FILE  /var/log/apache2.pid

RUN echo 'Hello, docker' > /var/www/index.html

ENTRYPOINT ["/usr/sbin/apache2", "-D", "FOREGROUND"]
#CMD ["-D", "FOREGROUND"]
