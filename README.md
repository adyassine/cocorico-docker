# dockernize cocorico
an environment based on docker and docker-compose to run cocorico plateform 
===========
* Clone the repo
    git clone [repo] cocorico

* Run docker-compose
    docker-compose run -d
    
To ssh on a running container
        docker exec -it [CONTANER_ID|CONTANER_NAME] /bin/bash  
    
* Stop all Docker containers 
    docker stop $(docker ps -a -q)