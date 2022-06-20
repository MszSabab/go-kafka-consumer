# KAFKA COMMANDS:

Segmentio/kafka-go is used to connect into Kafka
## Kafka shell: 
```bash
docker exec -it kafka /bin/sh
```

## Create topic from docker:
```bash
kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic <topic name>
```


## Partition add/alter:
```bash
kafka-topics.sh --alter --zookeeper zookeeper:2181 --partitions 2 --topic <topic name>
```


## List of topics:
```bash
kafka-topics.sh --list --zookeeper zookeeper:2181
```


## Producer from docker(proxy of producer sevrice):
```bash
kafka-console-producer.sh --broker-list localhost:9092 --topic <topic name>
```


## All message show from beginning:
```bash
kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic <topic name> --from-beginning
```