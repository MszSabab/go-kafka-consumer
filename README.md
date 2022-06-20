# KAFKA COMMANDS:

```bash
## Kafka shell: 
docker exec -it kafka /bin/sh
```
```bash
## Create topic from docker:
kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic <topic name>
```

```bash
## Partition add/alter:
kafka-topics.sh --alter --zookeeper zookeeper:2181 --partitions 2 --topic <topic name>
```

```bash
## List of topics:
kafka-topics.sh --list --zookeeper zookeeper:2181
```

```bash
## Producer from docker(proxy of producer sevrice):
kafka-console-producer.sh --broker-list localhost:9092 --topic <topic name>
```

```bash
## All message show from beginning:
kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic <topic name> --from-beginning
```