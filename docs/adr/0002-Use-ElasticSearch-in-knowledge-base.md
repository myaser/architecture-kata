# Use ElasticSearch for Knowledge base Component

## Context and Problem Statement
Adopting Microservice architecture allows us to mix technologies and choose the most suitable for each component. 
For the <i>Knowledge Base Component</i>, we considered few database options 

## Considered Options

* [Elasticsearch](https://www.elastic.co/elasticsearch/)
* [MongoDB](https://www.mongodb.com/)
* SQL Database

## Decision Outcome

Chosen option: Elasticsearch

* Better support for text search

### Positive Consequences

We assume that experts browsing the <i>Knowledge Base</i> are intrested in searching and filtring by ticket description as well. To avoid data coupling between <i>Knowledge Base Component</i> and <i>Ticket Component</i>, we serialize ticket information into a text field within Knowledge base records. Elasticsearch will allow us to search through the knowledge base and ticket desciption at the same time. 

