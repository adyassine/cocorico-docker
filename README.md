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

add market.local to the hosts file :

```bash
$ sudo vi /etc/hosts  # add 127.0.0.1 market.local
```

You should now install composer dependencies :

```bash
$ docker exec -it market_web composer install
```

To ssh on a running container :

```bash
$ docker exec -it [CONTANER_ID|CONTANER_NAME] /bin/bash 
```

Stop all Docker containers:

```bash
$ docker stop $(docker ps -a -q)
```