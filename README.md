# wellnite_project REST API Gateway + microservices

This project is a [monorepo](https://gomonorepo.org/) containing a REST API gateway with TCP back-end microservices all written using the NestJS Framework and TypeScript.

## Architecture Overview
 
The REST API acts as a gateway/proxy for the different microservices it exposes. The controllers of the REST API make calls to the TCP servers/microservices in the back-end. The TCP microservices then handles the request to connect to databases or any other service it needs to serve requests.

## Layers

### API Layer

[NestJS + Express](https://nestjs.com/) acts as the API Layer for the architecture. It takes care of listening for client requests and calling the appropriate back-end microservice to fulfill them.

### Microservice Layer

TCP was chosen as the framework to do the microservices.

### Persistence Layer

PostgreSQL is used as the database and TypeORM is used as the Object-Relational Mapper (ORM).

## How to Run

1. System Requirements - must be Linux/Mac
- [Node.js](https://nodejs.org/en/) - v12 Recommended

2. On the Terminal, go into the project's root folder (`cd /project/root/folder`) and execute `npm start`. The start script will install all npm dependencies for all projects.

3. Once the start script is done, the API Gateway will listening on [http://localhost:3000](http://localhost:3000)
