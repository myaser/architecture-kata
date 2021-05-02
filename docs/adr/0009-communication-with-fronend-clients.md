# Communication with frontend clients

## Context and Problem Statement
Events driven micro service architecture creates a challenge on the level of comunication with front-end. More precisely, how to associate results with user requests in an async environment with stateless services.

## Decision Outcome
* Communication between front-end and backend service will be ensured using socket.IO
* We can rely on socket.IO with sticky sessions and redis database (for saving user sessions) to ensure that results are forwaded to the relevant user


### Positive Consequences
* Using Async comunication between front-end and backend allows for displaying partial results whenever it make sense.
