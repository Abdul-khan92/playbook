FROM ubuntu 
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt-get update 
RUN apt-get install apache2 -y && apt clean 
RUN apt-get install apache2-utils -y
COPY index.html /var/www/html
EXPOSE 80
CMD ["apache2ctl", "-D", "FOREGROUND"]
