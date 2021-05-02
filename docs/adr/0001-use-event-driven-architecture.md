# Use Event Driven Architecture

## Context and Problem Statement

After we decided that we wanted to use microservice architecture, we needed to defined how would these services communicate


## Considered Options

* Event Driven
* Synchronous Rest API calls
* Mix of both

## Decision Outcome

Chosen option: "Event Driven", because:

* Offers an easy way to implement reporting across the system (By reading events from all the queues in the system)
* Flexibility: Adding new components and removing components are easier
* Monitoring: it's easier to monitor system performances and monitoring the deadletter queues and throughput make it easier to detect problems and to identify performance bottlenecks
* Testing and load testing is easier to implement

### Negative Consequences

* Using an event Broker introduces a single point of failure to the system but in practice event brokers such as AWS SQS, Kafka and RabbitMQ have proven to be very reliable in the past
* Debugging the system can be challenging but with the correct tools and monitoring this can be managed 

## Pros and Cons of the Options

### Synchronous Rest API calls

* Easier to implement 
* More coupling between services
* Monitoring HTTP calls between services is not as easy as monitoring events in queues

### Mix of both

* More complex to implement than just commiting to on of either solutions 
* Introduces more challenges for testing and monitoring
