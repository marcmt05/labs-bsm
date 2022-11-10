## Desde la imagen base de ubuntu
FROM ubuntu

# Actualizamos paqueteria
RUN apt update

ARG DEBIAN_FRONTEND=noninteractive

# Instalamos apache2
RUN apt install apache2 -y
RUN apt install apache2-utils -y
RUN apt clean 

# Configuramos apache 2
ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

# Indica cómo funciona el contenedor en el puerto 80 y con el comando apache2ctl
EXPOSE 80
CMD ["apache2ctl", "-D", "FOREGROUND"]