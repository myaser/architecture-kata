# Use of RabbitMQ

With decision of using an event driven architecture, a follow up decision rises. Which event broker to choose. Different Event brokers support different functionalities that do affect architectural decisions.

## Considered Options

* [RabbitMQ](https://www.rabbitmq.com/)
* [Kafka](https://kafka.apache.org/)
* [AWS SQS](https://aws.amazon.com/sqs/)

## Decision Outcome

Chosen option: RabbitMQ, because

* Ability to take advantage of the different routing logic in RabbitMQ exchanges makes it possible to simplify clients. (Simpler clients are easier to test and maintain)
* Variety of publish/subscribe, point-to-point request/reply messaging capabilities adds multiple options for developers to implement an event driven architecture with ease
* Although performance wise, RabbitMQ have less throughput than other technologies that we took in consideration, we think that the performance will be sufficient for our system
* No vendor lock-in
