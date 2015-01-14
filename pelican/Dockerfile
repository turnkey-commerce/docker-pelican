FROM python:2.7
MAINTAINER James Culbertson <info@turnkey-commerce.com>
ENV REFRESHED_AT 2015-01-11

# Update OS
RUN sed -i 's/# \(.*multiverse$\)/\1/g' /etc/apt/sources.list
RUN apt-get update
RUN apt-get -y upgrade

RUN mkdir /pelican

COPY ./Makefile /pelican/Makefile
COPY ./pelicanconf.py /pelican/pelicanconf.py
WORKDIR /pelican

# Pelican
RUN pip install pelican Markdown
RUN git clone https://github.com/DandyDev/pelican-bootstrap3.git /pelican-bootstrap3
VOLUME /var/www/html

CMD  ["make","regenerate"]