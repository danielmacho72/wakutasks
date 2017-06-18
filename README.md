# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

Dev Environment is generated using docker:

To build and run individual docker image for application (not including dependencies)

  $ docker build -t wakutasks .
  $ docker run -p -v <fully_qualified_path_to>/wakutasks:/usr/src/app <host_port>:3000 wakutasks

However, please use docker-compose to run all dependencies using their own containers

  $ docker-compose up 

First time you run all images are built, following times you need to explicitly request them to be built

Use `docker-compose build` or `docker-compose up --build`

* ...
