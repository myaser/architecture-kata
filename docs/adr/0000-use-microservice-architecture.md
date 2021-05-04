# Use Microservice Architectural

## Context and Problem Statement

Considering the functional and non functional requirements, we set up to choosing a suitable architecture

## Considered Options

* Monolith Architecture
* Microservice Architecture
* [Serverless Architecture](https://aws.amazon.com/lambda/serverless-architectures-learn-more/)

## Decision Outcome

Chosen option: "Microserive Architecture" for the following reasons:

* Scalibility: Horizantal scalabity is easy to implement
* Adaptive and Dynamic: change is fairly easy to implement and integrate
* Availability: Replication and no single point of failure make it possible to ensure high availability
* Elasticity: System can be scaled up and down depending on the usuage
* Ability to integrate different technologies

### Negative Consequences

* More complex to implement
* Data consistency and transaction management is a challenge 

## Pros and Cons of the Options

### Monolith architecture

* Codebase gets cumbersome over time
* Limited agility
* Simpler development and deployment

### Serverless Architecture

* Higher reliability
* Lower costs
* Easy to deploy
* Vendor lock-in
* Difficult to evaluate long term
