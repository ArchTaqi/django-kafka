# NodeJs Kafka


## Setup

```bash
docker run -p 2181:2181 zookeeper
# get ur IP Address
docker run -p 9092:9092 \
-e KAFKA_ZOOKEEPER_CONNECT=192.168.18.50:2181 \
-e KAFKA_ADVERTISED_LISTENERS=PLAINTEXT://192.168.18.50:9092 \
-e KAFKA_OFFSETS_TOPIC_REPLICATION_FACTOR=1 \
confluentinc/cp-kafka
```

## Running

```bash
node admin.js
node consumer.js <GROUP_NAME>
node producer.js
```

