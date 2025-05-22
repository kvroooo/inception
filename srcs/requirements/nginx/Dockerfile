FROM debian:bullseye

RUN apt update && apt install nginx -y \
	&& apt install curl -y && apt install vim -y \
	&& apt install openssl -y && mkdir -p /etc/nginx/ssl \
	&& apt install nano -y

COPY /conf/nginx.conf /etc/nginx/nginx.conf

