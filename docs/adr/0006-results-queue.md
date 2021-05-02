# Results Queue

## Context and Problem Statement
The use of event driven Architecture create the challenge of reporting success and errors that happen asynchronously to users


## Decision Outcome
* Use a dedicated Queue (<i>Results Queue </i>) that containes all of the generated success messages with requested data if any and error messages
* Use a request-ID property that will allow the front-end appliations to match the result events with the corresponding user actions and display the results correctly 

<-- ADD DIAGRAM HIGHLIGHTING SOLUTION -->


### Positive Consequences

* Allows front-end application to display partial results whenever it make sense. This can make the user perceive the system as fast when implemented well.
* Integrating and removing services is simpler task
* Keeping track of the request-ID is a good way to monitor system health and can be leveraged with the use of some monitoring tools to visualize and trace the flow of data accross the system
