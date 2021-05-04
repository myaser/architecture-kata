# Subscription Order transaction

## Context and Problem Statement
The use of multiservice architecture creates the problem of executing transations across multiple components. One examples of these transaction is the subscription.

<-- TODO ADD seq diagram highlighting the problem -->

<-- TODO ADD component diagram highlighting the problem-->


## Decision Outcome
First step to solve this problem is :

* We decided to merge the <i>Support Plan Component </i> (the component that tracks the support plans provided by the company) and the <i> Orders Component </i> ( the component keeping track of which customer is subscribed to which Support Plan )
* Those two components had a lot of coupling between them. Making them into a single component allows for easier maintance and developement.
* Allows for better handling of transactions 
* Avoid edge cases that can make data inconsistent

Second Step is:

* Implement choreography saga between the <i>Support Plan/Orders Component </i> and <i> Payment Component </i> 
<-- ADD DIAGRAM HIGHLIGHTING CHOREOGRAPHY -->


### Positive Consequences

These changes allows for very flexible architecture: 

* Different payment method can be implemented and changed and the component that needs to be modified is the <i>payment component </i> 
* Support plans can have different subsription plans (different payment periods) and this logic is contained within <i>Support Plan/Orders Component </i> alone
* Support plans can have limits of number of subcriptions and this logic is contained within <i>Support Plan/Orders Component </i> alone
