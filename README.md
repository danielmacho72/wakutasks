# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

Environment variables that you need to setup before you run in any environment:

> e.g to setup your environment variables for MAC OSX update your ~/.bash_profile as follows:

```
export POSTGRES_PASSWORD="yoursecretpassword"
export SMARTHOST_ADDRESS=smtp.mandrillapp.com
export SMARTHOST_PORT=587
export SMARTHOST_USER=<mandrillapp_user>
export SMARTHOST_PASSWORD=<mandrillapp_token>
```

Note: you will need to setup an account in mandrill or use your own SMTP provider 

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

Run your Dev Environment using docker:

You will need to download docker

To build and run individual docker image for application (not including dependencies)

  * `$ docker build -t wakutasks .`
  * `$ docker run -p -v <fully_qualified_path_to>/wakutasks:/usr/src/app <host_port>:3000 wakutasks`

However, please use rather docker-compose to run all dependencies using their own containers

  * `$ docker-compose up`
  * `$ docker-compose run web rake db:create`

Once running you can access the application via localhost:5002

NOTE: First time you run all images are built, following times you need to explicitly request them to be built

Use `docker-compose build` or `docker-compose up --build`

* ...
