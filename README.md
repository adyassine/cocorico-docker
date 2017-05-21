#  Dockernize Cocorico 

An environment based on docker and docker-compose to run cocorico plateform  [Cocorico](https://github.com/Cocolabs-SAS/cocorico).


## Setup

First, clone the latest version of Cocorico

```bash
$ cd ./www
$ git clone https://github.com/Cocolabs-SAS/cocorico.git
```

Then start containers (databases and web) with docker-compose :

```bash
$ docker-compose up -d
```

You should now install composer dependencies :

```bash
$ docker exec -it market-web composer install
```

To ssh on a running container :

```bash
$ docker exec -it [CONTANER_ID|CONTANER_NAME] /bin/bash 
```

Stop all Docker containers:

```bash
$ docker stop $(docker ps -a -q)
```