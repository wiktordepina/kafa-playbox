# kafka-playbox

## Setup:
```shell
brew bundle
```

## Run:
1. To start kafka cluster in docker: `docker-compose up kafka-cluster`
2. To check if cluster is running correctly: `docker-compose ps`
3. To run a producer `./start_producer.sh`
4. To run an independent consumer: `./start_consumer.sh`
5. To start a consumer in a consumer group: `./start_consumer_in_group.sh`
6. To stop kafka cluster `docker-compose down`


## Usefull commands:
1. List topics:
```shell
kafka-topics --bootstrap-server localhost:9092 --list
```

2. Create topic:
```shell
kafka-topics --bootstrap-server localhost:9092 --create --topic ids [--partitions <number_of_partitions>]
```

3. Start producer:
```shell
kafka-console-producer --bootstrap-server localhost:9092 --topic <topic_name>
```

4. Start consumer:
```shell
kafka-console-consumer --bootstrap-server localhost:9092 --topic <topic_name> [--group <consumer_group_id>]
```

5. List consumer groups:
```shell
kafka-consumer-groups --bootstrap-server localhost:9092 --list
```
