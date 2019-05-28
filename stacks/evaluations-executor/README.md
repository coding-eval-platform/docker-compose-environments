# Evaluations and Executor Services

Stack that allows running the [Evaluations Service](https://github.com/coding-eval-platform/evaluations-service) together with the [Executor Service](https://github.com/coding-eval-platform/executor-service), using Kafka to communicate between themselves.

## Components

- Apache Zookeeper
- Apache Kafka
- PostgreSQL database
- Evaluations Service
- Nginx reverse proxy

## Variables

The following table contains the variables that are used by the ```docker-compose.yml``` file.
Those without a default value must be set using the ```export``` command.


| Variable                              | Description                                       | Default value         |
|:--------------------------------------|:--------------------------------------------------|:---------------------:|
| EVALUATIONS_SERVICE_VERSION           | The Evaluations Service Docker image tag          | 0.1.0-RELEASE         |
| EVALUATIONS_SERVICE_POSTGRES_USER     | The Evaluations Service database username         | evaluations-service   |
| EVALUATIONS_SERVICE_POSTGRES_PASSWORD | The Evaluations Service database user's password  | evaluations-service   |
| EVALUATIONS_SERVICE_POSTGRES_DATABASE | The Evaluations Service database name             | evaluations-service   |
| EXECUTOR_SERVICE_VERSION              | The Executor Service Docker image tag             | 0.0.1-RELEASE         |


## Example

The following is a full example that indicates how to run the stack.

```
$ docker-compose up
```
