# CQRS (Command Query Responsibility Segregation) with Java Microservice & Kafka

## Use Case: Bank Account Creation & Querying

This project demonstrates a microservice implementation of Bank account creation and querying using **CQRS** design pattern

## Concepts

### CQRS (Command Query Responsibility Segregation)

**Command Query Responsibility Segregation (CQRS)** is a design pattern in information technology that separates the concerns of writing data (commands) from reading data (queries). CQRS can help improve performance, scalability, and security. It's often used in mission-critical systems, collaborative domains, and systems that are expected to evolve over time
In a CQRS system, there are separate interfaces for sending queries and commands. Commands are issued when a user wants to modify the system's state, and they can be processed immediately or queued for later processing. Because commands and queries often have different performance characteristics and scalability requirements, CQRS allows microservices to be independently scaled based on the workload they handle.

### Apache Kafka + Zookeeper

![Apache Kafka + Zookeeper diagram](/docs/kafka-zookeeper.png)

**Kafka** is a distributed event store and streams-processing platform, meaning simply it takes data from producers and streams them out to consumers.

**Kafka Brokers**: A Kafka broker is a single instance or node in the Kafka system. It is in charge of receiving incoming messages, storing them, and serving them to consumers

**Kafka Cluster**: A cluster is a set of Kafka brokers that interact with each other

**Kafka Topic**: Kafka topics are the categories used to organize messages. Each topic has a name that is unique across the entire Kafka cluster. Messages are sent to and read from specific topics. In other words, producers write data to topics, and consumers read data from topics. Kafka topics are multi-subscriber.

**Apache Zookeper**: To coordinate all the data flow between consumers, producers, and brokers, Kafka leverages Apache ZooKeeper. Its a control plane, a centralized service that manages metadata in Apache Kafka clusters, providing distributed coordination, naming, and configuration information