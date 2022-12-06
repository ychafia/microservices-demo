# Microservices commands 
Please find here some commands to start microservices :
## start docker compose :
- cd docker-compose br
- docker-compose -f common.yml -f kafka_cluster.yml up

## list docker containers :
- docker ps

## Use kafkacat tool from docker container :
- docker run -it --network=host confluentinc/cp-kafkacat kafkacat -L -b localhost:**`29092`**

## connect to docker container terminal :
- docker exec -it **`298fd418f85f`**  bash 
