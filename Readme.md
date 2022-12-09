# Microservices commands 
Please find here some commands to start microservices :
## start docker compose :
- cd docker-compose br
- docker-compose -f common.yml -f kafka_cluster.yml up
    #### update :
    After transformate twitter-to-kafka-service to a dokcer image, you simplu user dokcer-compose to start all service inside docker containers
    - docker-compose -f common.yml -f kafka_cluster.yml -f services.yml up
    - OR
    - docker-compose up

## list docker containers :
- docker ps

## Use kafkacat tool from docker container :
- docker run -it --network=host confluentinc/cp-kafkacat kafkacat -L -b localhost:**`29092`**
## List messages (events) inside _twitter-topic_ :
- docker run -it --network=host confluentinc/cp-kafkacat kafkacat -b localhost:19092 -t twitter-topic

## connect to docker container terminal :
- docker exec -it **`298fd418f85f`**  bash 
