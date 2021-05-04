# Reporting architectural decisions

One requirement for the project is to allow managers access to performance, financial and operational reporting

## Considered Options

* Add reporting functionalities to each component (ability to list, filter and aggregate results)
* Implement reporting as stand alone component and use third party reporting tool (Tableau, QlickView, etc..)

## Decision Outcome

Chosen option: Implement reporting as stand alone component 

* The use of event driven microservice architecture allow us to listen to all events in the system and use a <i>Reporting Adapter Component</i> that will extract, transform and save the desired data in a specialized database
* This will allow to seperate analytical data and operational data in a way that allows us to receive a close to real time reporting
* A reporting tool (Tableau, QlickView, etc..) can be leveraged to provide the required reporting generated from database
* This will be more effective and a lot simpler than building our own reporting

### Positive Consequences

* Seperate operational and analytical data
* Decoupling of the reporting module from the rest of the system
* The use of a single database specialized for reporting allows for simpler generation and maintainance of reports and better performances
* The use of third party tools to generate reports allows for more dynamic and powerful reporting

### Negative consequences

* The <i>Reporting Adapter Component</i> will be a concern whenever an event structure changes
* We introduce the risk of the reported data to be different than the operational data

## Pros and Cons of the Options

### Add reporting functionalities to each component
* Reporting will always be accurate
* Added complexity to each component
* Accomodating both operational and analytical use cases can lead to overall worse performances ( for example too many indexes will need to be defined )
