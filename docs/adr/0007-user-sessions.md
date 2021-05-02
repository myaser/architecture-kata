# User Sessions

## Context and Problem Statement
With the presence of multiple roles. Role based access system needs to be in place. 

## Considered Options
* Ensure different authentication/authorization component for <b>each</b> access role
* Use the same authentication/authorization component for <b>all</b> access role

## Decision Outcome
* Use a dedicated component that validates access rights and that the user is authorized to generate the event
* Associates user-ID with the generated event. Allowing other services to trust this field
* Filters the results generated in the <i>Results Queue</i> and ensures that it's only delivered to the authorized users

<-- ADD DIAGRAM HIGHLIGHTING SOLUTION -->


### Positive Consequences

* Handling authentication/authorization of all users in a single component make it easier to maintain

