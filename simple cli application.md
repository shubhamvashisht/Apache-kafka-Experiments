# A simple CLI based demonstraion of Apache-Kafka. 
### We will create a simple CLI based app to demonstrate transfer of messages between a producer and a consumer.
1. Download and Install Apache-kafka from [here](https://www.apache.org/dyn/closer.cgi?path=/kafka/1.0.0/kafka_2.11-1.0.0.tgz).
2. Start the zookeeper server by executing `/bin/zookeeper-server-start.sh config/zookeeper.properties`.
3. Start the main kafka server by executing `bin/kafka-server-start.sh config/server.properties`.
4. create a topic (Category) in order to link messages with it by executing `bin/kafka-topics.sh --create --zookeeper localhost:3211 --replication-factor 1 --partitions 1 --topic Kafkaexperiments`.
5. Now create a simple consumer which can listen to/consume messages for the topic we created by executing `bin/kafka-console-consumer.sh --zookeeper localhost:3211 --topic Kafkaexperiments --from-beginning`.
6. We have a consumer which will listen to the messages belong to a particular topic , now we need a producer to generate messages.
7. create a simple producer that can publish messages by executing `bin/kafka-console-producer.sh --broker-list localhost:9000 --topic Kafkaexperiments`.
Thats it.
Now we can test if everything is working fine by entering a message in the producer console which should be appear on consumer console at once.
Example.
![Consumer & Producer console](/extras/images/ApacheKafkaCLI.png)
