# docker-pelican
Docker and Fig containers for Pelican static site generation, served by Nginx.

This project creates two Docker containers, one for the Pelican blog static file blog generator and another for the serving of the content using an Nginx contrainer.  Fig is used to orchestrate the building of the images and running of the containers.

To Install:

1. Install [Docker](https://docs.docker.com/) on a Linux box or VM.
2. Install [Fig](http://www.fig.sh/install.html).

To start:

1. fig build
2. fig up -d

To stop:

1. fig stop

To add more content add Markdown (.md) or reStructuredText (.rst) files to the content folder and the blog will automatically be regenerated on change. For more information check the [Pelican documentation](http://docs.getpelican.com/en/latest/index.html). 