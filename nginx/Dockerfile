FROM nginx
MAINTAINER James Culbertson <info@turnkey-commerce.com>
ENV REFRESHED_AT 2015-01-11

# Update OS
RUN sed -i 's/# \(.*multiverse$\)/\1/g' /etc/apt/sources.list
RUN apt-get update
RUN apt-get -y upgrade

# nginx specific
VOLUME /var/www/html
WORKDIR /var/www/html

RUN rm /etc/nginx/conf.d/default.conf
COPY ./default.conf /etc/nginx/conf.d/default.conf