# Project ACME

The objective of the project is to re-engineer the ACME application adopting the approach of a decentralized/distributed system.

This project was developed for evaluation in the Systems Integration course of the Master in Informatics Engineering - Software Engineering at Instituto Superior de Engenharia do Porto - ISEP/IPP

#### Two dimensions of decentralization/distribution are addressed:
- Business Domain Segregation: The monolithic application was segregated into three distinct but collaborative applications:
    - Products
    - Reviews
    - Votes

- Cloning: Multiple instances of each of the above applications are deployed in containers.
## Requirements
### Non-functional requirements
- Deployment must be automated through CI/CD.
- Adoption of service component test pattern.
- Adoption of end-to-end test pattern.
- Two or more frameworks/programming languages must be adopted in implementing the services.
- AMQP Message Broker (e.g. RabbitMQ) must be adopted for communication between services.

### Functional requirements
- Endpoint in service Votes that allows creating a vote for a non-existing review. The review must be created for the specified product, and the vote is eventually associated with the review.

- Develop a bootstrap process for the starting services. I.e. at any time, a new service can start and its data must be bootstrapped.

#### The following patterns must be adopted:
- Strangler fig
- Command-Query Responsibility Segregation (CQRS)
- Database-per-Service
- Polyglot persistence
- Messaging (RabbitMQ - AMQP Message Broker)
- The Domain Events
- Event Sourcing
- Saga
## Tools
- Docker
- RabbitMQ
- H2

## Programming Language

- Java (Spring Boot)
- PHP
## Features

- Load Balance
- Discovery System
- Message Broker (RabbitMQ)
- Bootstrap
- Product, Review e Votes (Command/Query)

## Students
| <img alt="@DavidGomesh" src="https://avatars.githubusercontent.com/DavidGomesh?size=64" style="border-radius: 50%;"> | <img alt="@RegianaBarbosa" src="https://avatars.githubusercontent.com/RegianaBarbosa?size=64" style="border-radius: 50%;"> |
| :-: | :-: |
| *David Gomes* | *Regiana Barbosa* |

## Professor
| <img alt="@NunoSilva" src="https://avatar-management--avatars.us-west-2.prod.public.atl-paas.net/557058:6fcae13e-78be-47ae-b86f-32c59404c8a3/de6bf548-8908-4c59-bdac-2813d38f37a0/64" style="border-radius: 50%;"> |
| :-: |
| *Nuno Silva* |