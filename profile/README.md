# Project ACME

The objective of the project is to re-engineer the ACME application adopting the approach of a decentralized/distributed system.

This project was developed for evaluation in the Systems Integration course of the Master in Informatics Engineering - Software Engineering at Instituto Superior de Engenharia do Porto - ISEP/IPP

#### Two dimensions of decentralization/distribution are addressed:
- Business Domain Segregation: The monolithic application was segregated into three distinct but collaborative applications:
    - Products
    - Reviews
    - Votes

- Cloning: Multiple instances of each of the above applications are deployed in containers.

<br>

## Requirements

### Non-functional requirements
- Deployment must be automated through CI/CD.
- Adoption of service component test pattern.
- Adoption of end-to-end test pattern.
- Two or more frameworks/programming languages must be adopted in implementing the services.
- AMQP Message Broker (e.g. RabbitMQ) must be adopted for communication between services.

<br>

### Functional requirements
- Endpoint in service Votes that allows creating a vote for a non-existing review. The review must be created for the specified product, and the vote is eventually associated with the review.

- Develop a bootstrap process for the starting services. I.e. at any time, a new service can start and its data must be bootstrapped.

<br>

### _The following patterns must be adopted_:
- Strangler fig
- Command-Query Responsibility Segregation (CQRS)
- Database-per-Service
- Polyglot persistence
- Messaging (RabbitMQ - AMQP Message Broker)
- The Domain Events
- Event Sourcing
- Saga
- CI (Continuous Integration)

<br>

## Tools

- Docker
- RabbitMQ
- H2
- MongoDB
- Axon Server
- Eureka (Netflix)
- Git/GitHub
- GitHub Actions (CI)

<br>

## Programming Language

- Java (JDK 17)
- Node.js

<br>

## Features

- Load Balance
- Discovery System
- Message Broker (RabbitMQ)
- Bootstrapper
- Product, Review e Vote (Command/Query)

<br>

# Documentation
## Logic View
![logic view image](docs/ACME-logic-view.svg)

## Physical View
![physical view image](docs/ACME-physical%20view.svg)

## Sequence Diagrams
### Case 01 POST Product
![case01-post-product](docs/ACME-Case%2001%20HttpClient%20POST%20Product%20Request.svg)

<br>

### Case 02 POST Review
![case02-post-review](docs/ACME%20-Case%2002%20HttpClient%20POST%20Review%20Request.svg)

<br>

### Case 03 POST Vote
![case03-post-vote](docs/ACME-Case%2003%20HttpClient%20POST%20Vote%20Request.svg)

<br>

### Case 04 SAGA
![case04-saga](docs/ACME-Case%2004(SAGA).svg)
<br>

<br>

## Students
| <img alt="@DavidGomesh" src="https://avatars.githubusercontent.com/DavidGomesh?size=64"> | <img alt="@RegianaBarbosa" src="https://avatars.githubusercontent.com/RegianaBarbosa?size=64"> | <img alt="@NaironCarneiro" src="https://avatars.githubusercontent.com/NaironCarneiro?size=64"> |
| :-: | :-: | :-: |
| *David Gomes* | *Regiana Cruz* | *Nairon Carneiro* |

## Professor
| <img alt="@NunoSilva" src="https://avatar-management--avatars.us-west-2.prod.public.atl-paas.net/557058:6fcae13e-78be-47ae-b86f-32c59404c8a3/de6bf548-8908-4c59-bdac-2813d38f37a0/64"> |
| :-: |
| *Nuno Silva* |
