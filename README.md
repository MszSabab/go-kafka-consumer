### KAFKA COMMANDS
kafka shell: 
docker exec -it kafka /bin/sh


create topic from docker:
kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic <topic name>


partition add/alter:
kafka-topics.sh --alter --zookeeper zookeeper:2181 --partitions 2 --topic <topic name>


list of topics:
kafka-topics.sh --list --zookeeper zookeeper:2181


producer from docker(proxy of producer sevrice):
kafka-console-producer.sh --broker-list localhost:9092 --topic <topic name>


all message show from beginning:
kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic <topic name> --from-beginning
