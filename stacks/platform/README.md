# Platform

Stack that allows running the whole platform.

## Components

- Apache Zookeeper
- Apache Kafka
- PostgreSQL database
- Evaluations Service
- Playground Service
- Executor Service
- Service Registry
- API Gateway

## Variables

The following table contains the variables that are used by the ```docker-compose.yml``` file.
Those without a default value must be set using the ```export``` command.


| Variable                              | Description                                       | Default value         |
|:--------------------------------------|:--------------------------------------------------|:---------------------:|
| API_GATEWAY_VERSION                   | The API Gateway Docker image tag                  | -                     |
| EVALUATIONS_SERVICE_VERSION           | The Evaluations Service Docker image tag          | -                     |
| EVALUATIONS_SERVICE_POSTGRES_USER     | The Evaluations Service database username         | evaluations-service   |
| EVALUATIONS_SERVICE_POSTGRES_PASSWORD | The Evaluations Service database user's password  | evaluations-service   |
| EVALUATIONS_SERVICE_POSTGRES_DATABASE | The Evaluations Service database name             | evaluations-service   |
| PLAYGROUND_SERVICE_VERSION            | The Playground Service Docker image tag           | -                     |
| PLAYGROUND_SERVICE_POSTGRES_USER      | The Playground Service database username          | playground-service    |
| PLAYGROUND_SERVICE_POSTGRES_PASSWORD  | The Playground Service database user's password   | playground-service    |
| PLAYGROUND_SERVICE_POSTGRES_DATABASE  | The Playground Service database name              | playground-service    |
| EXECUTOR_SERVICE_VERSION              | The Executor Service Docker image tag             | -                     |
| SERVICE_REGISTRY_VERSION              | The Service Registry Docker image tag             | -                     |


**Note:** In fact, there are default values for all the Docker images, but they are snapshot builds.


## Example

The following is a full example that indicates how to run the stack.

```
$ export API_GATEWAY_VERSION=...
$ docker-compose up
```
