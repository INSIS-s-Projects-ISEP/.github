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

**Non-functional requirements**
- Deployment must be automated through CI/CD.
- Adoption of service component test pattern.
- Adoption of end-to-end test pattern.
- Two or more frameworks/programming languages must be adopted in implementing the services.
- AMQP Message Broker (e.g. RabbitMQ) must be adopted for communication between services.

<br>

**Functional requirements**
- Endpoint in service Votes that allows creating a vote for a non-existing review. The review must be created for the specified product, and the vote is eventually associated with the review.

- Develop a bootstrap process for the starting services. I.e. at any time, a new service can start and its data must be bootstrapped.

<br>

*The following patterns must be adopted:*
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
![logic view image](https://raw.githubusercontent.com/INSIS-s-Projects-ISEP/.github/main/profile/docs/ACME-logic-view.svg)

## Physical View
![physical view image](https://raw.githubusercontent.com/INSIS-s-Projects-ISEP/.github/main/profile/docs/ACME-physical%20view.svg)

## Sequence Diagrams
### POST Product
![case01-post-product](https://raw.githubusercontent.com/INSIS-s-Projects-ISEP/.github/main/profile/docs/ACME-Case%2001%20HttpClient%20POST%20Product%20Request.svg)

<br>

### POST Review
![case02-post-review](https://raw.githubusercontent.com/INSIS-s-Projects-ISEP/.github/main/profile/docs/ACME%20-Case%2002%20HttpClient%20POST%20Review%20Request.svg)

<br>

### POST Vote
![case03-post-vote](https://raw.githubusercontent.com/INSIS-s-Projects-ISEP/.github/main/profile/docs/ACME-Case%2003%20HttpClient%20POST%20Vote%20Request.svg)

<br>

### SAGA
![case04-saga](https://raw.githubusercontent.com/INSIS-s-Projects-ISEP/.github/main/profile/docs/ACME-Case%2004(SAGA).svg)

<br>

<br>

# Starting services locally with docker-compose
This tutorial will guide you through the installation and execution of the services required to start your application locally with docker-compose.

<br>

## Prerequisites
- [Docker Engine](https://www.docker.com/products/docker-desktop/) installed.
- Sufficient hardware and software resources to support the execution of all applications simultaneously without causing performance or stability issues.
    - Applications:
        * discovery-system
        * load-balancer
        * axonserver
        * product-command
        * product-command-bootstrapper
        * product-query
        * product-query-bootstrapper
        * review-command
        * review-command-bootstrapper
        * review-query
        * review-query-bootstrapper
        * vote-command
        * vote-command-bootstrapper
        * vote-query
        * vote-query-bootstrapper

<br>

## Step-by-step
1. Open Docker to view the applications.

2. Download the [docker-compose.yml](https://github.com/INSIS-s-Projects-ISEP/.github/blob/main/profile/docs/docker-compose.yml) file required to start the services locally.

3. Open a terminal and navigate to the directory where the [docker-compose.yml](https://github.com/INSIS-s-Projects-ISEP/.github/blob/main/profile/docs/docker-compose.yml) file is saved. Then, execute the following command to start the services in the background: 
```
docker-compose up -d
```

4. Wait for all services to start. You can check the status of the services using the `docker-compose ps` command.

5. To access the services, use the following links:

- Discovery System (Eureka Server): http://localhost:8761
- Message Broker: http://localhost:15672
- Axon Server (Event Sourcing): http://localhost:8024

<br>

## Stopping the services
You can stop the services at any time by using the `docker-compose down` command in the directory where the `docker-compose.yml` file is saved.

<br>

## Conclusion
Now you can use the services locally with docker-compose. Make sure the services are stopped before running the application in another environment. If you have problems during installation or execution, make sure you followed the steps described in this tutorial correctly and that all prerequisites were met.

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