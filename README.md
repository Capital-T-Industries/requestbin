# We have discontinued the publicly hosted version of RequestBin due to ongoing abuse that made it very difficult to keep the site up reliably. Please see instructions below for setting up your own self-hosted instance.

Originally Created by [Jeff Lindsay](http://progrium.com)

License
-------
MIT


Looking to self-host?
=====================

## [Deploy your own instance using Heroku](https://github.com/Runscope/requestbin#deploy-your-own-instance-using-heroku)

## [Deploy your own instance using Docker](https://github.com/Runscope/requestbin#deploy-your-own-instance-using-docker)

## Run a prebuilt Docker image hosted on Docker Hub

Run an instance of the RequestBin docker image hosted on [Docker Hub](https://hub.docker.com/r/clarketm/requestbin/); specify the desired port to expose on your server/machine: 

#### 1. Create a network
```bash
$ docker network create requestbin
```

#### 2. Run a redis instance on the network
```bash
$ docker run --name redis --network requestbin redis -d
```

#### 3. Run a requestbin instance on the network
```bash
$ PORT=8000
$ docker run --name requestbin -p $PORT:8000 --network requestbin clarketm/requestbin -d
```

Your own private RequestBin instance will be running on the specified port (e.g. http://localhost:8000).

## Run with a single command using Docker-Compose
```bash
$ docker-compose -f <(curl "https://raw.githubusercontent.com/Capital-T-Industries/requestbin/master/docker-compose.yml") up -d
```

Contributors
------------
 * Barry Carlyon <barry@barrycarlyon.co.uk>
 * Jeff Lindsay <progrium@gmail.com>
 * Travis Clarke <travis.m.clarke@gmail.com>
