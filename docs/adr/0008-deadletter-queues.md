# Dead Letter Queues

## Context and Problem Statement
Multiple queues like the <i>results</i> queue can become a single point of failure and that can happen in cases when for example a message is malformed and connot be processed by the consumers.

## Decision Outcome
The use of dead letter queues provided by RabbitMQ, allows message to be transfered to a seperate queue after failing multiple times


### Positive Consequences

* This allows detection of system anomalies and generating alerts 
* replaying events without the loss of data after fixing the error
