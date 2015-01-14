# docker-pelican
Docker and Fig containers for Pelican static site generation, served by Nginx.

This project creates two Docker containers, one for the Pelican blog static file blog generator.  Fig is used to orchestrate the building of the image and running of the containers.

To start:

1. fig build
2. fig up -d

To stop:

1. fig stop
