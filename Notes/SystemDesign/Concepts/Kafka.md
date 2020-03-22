<h1>KAFKA</h1>

Kafka is a distributed streaming platform that is used for publish and subscribe 
to the stream of records

* Kafka is fast and used IO efficiently by batching and compressing records.

* Kafka is used for decoupling data records

* Kafka is used to stream data into data lakes, applications and real time stream analytics systems.

* Kafka clusters retain all published record. If you dont set a limit it will keep records until it runs out of disk space.

* kafka is Scalable Message Storage


<h2>KAFKA COMPONENTS</h2>
 * Producer: It send data, message, file
 * Consumer: 
    - It receive data
    - Producer just send the data to kafka server & any consumer can subscribe from kafka server. Consumer keeps on requesting data from server.
 * Broker:
    - Producer & consumer interact through Broker or kafa server
 * Cluster:
     - Kafka is distributed system, so cluster have many brokers
 * Topic: 
    - It's for identification for uniquely identify stream.
    - i.e we created Global Orders topic is created, Now consumer can subcribe to this topic
 * Partition: 
    - Break Kakfa topic to multiple partition & store one partition on one cumputer
    - It's upon us to decide how many partition can be there. 
 * Offset: 
     - It's sequence id given to message as they arrive in partition
    - Topic name - Partition Number - Offset can locate exact message
 * Consumer Group:
    - Group of consumer who share the same workaround
    - It's for scalibility