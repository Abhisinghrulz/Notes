<h1>Message Queue</h1>

What is Message Queue?
Asynchronous service-to-service communication used in serverless and microservices architectures.

Message Queue -> Kafka

Publish all messages to kafka, and kafka will notify the consumers

How Message Queue Works?

* Message are stored on the queue by Producer until they are processed by Consumer and deleted.
* Each message is processed only once, by a single consumer.
* Queues are also used as fault tolerance, in case of any service outage, they can retry the requests.

Examples of message queue
Kafka, RabbitMQ