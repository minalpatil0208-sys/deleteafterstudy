
FROM ubuntu:latest

LABEL author "dev anup"

RUN apt-get update &&\
    apt-get install apache2 unzip -y

ADD https://templatemo.com/download/templatemo_580_woox_travel /var/www/html/templatemo_580_woox_travel.zip

RUN rm -rf /var/www/html/ index.html &&\
    unzip /var/www/html/ templatemo_580_woox_travel.zip -d /var/www/html/ &&\
    mv /var/www/html/templatemo_580_woox_travel/* /var/www/html/

EXPOSE 80

CMD ["apachectl" ,"-D", "FOREGROUND"]