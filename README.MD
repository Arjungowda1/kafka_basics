# Apache Kafka Basics

Enables realtime data streaming and provides a centralized management system reducing the number of connections between client and server

### Components

1. **Producer** : Source of realtime data who publishes realtime data
2. **Consumer** : Destination of realtime data that consumes data
3. **Kafka Server / Broker** : Intermediate that stores messages and facilitates communication between Producer and Consumer
4. **Cluster** : set of brokers (like scaling servers)
5. **Topic** : categorize types of messages (type of data - payments, bookings, etc). Consumer can subscribe to specific topic.
6. **Partitons** : break topics into multiple parts and save in multiple systems. Improves performance and reduce downtime.
7. **Offset** : sequence of topics and used to keep track of data that is already consumed and in case of downtime, consumer can start reading data from x offset.
8. **Consumer groups** : scaling consumer and define it as a consumer group and the work can be distributed among the consumers increasing the throughput. (_1-1 mapping happens between consumer and partition_)
9. **Zookeeper** : Keeps track of everything in kafka (_a log stream similar to cloudwatch_).


### Installation

> Flavors of Kafka
> - Open Source Apache Kafka
> - Commercial Distribution Confluent Kafka
> - Managed Kafka Confluent and AWS MSK
> 

------------------------------------
#### Apache Kafka v3.8.0
------------------------------------
1. Download: [Kafka](https://downloads.apache.org/kafka/3.8.0/kafka_2.12-3.8.0.tgz)

2. Starting Zookeeper: default port is 2181

    _keep the kafka files in first level of the drive or you can get "command line too long" error in windows_
    > cd /path/to/kafka <br>
    > \path\to\bin\zookeeper-server-start.bat  \config\zookeeper.properties

3. Start kafka server:
    > cd /path/to/kafka <br>
    > .\bin\windows\kafka-server-start.bat .\config\server.properties
