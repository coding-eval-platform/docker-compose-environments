# Platform

Stack that allows running the whole platform.

## Components

- Apache Zookeeper
- Apache Kafka
- PostgreSQL database
- LTI Service
- LTI App
- Users Service
- Evaluations Service
- Playground Service
- Executor Service
- Service Registry
- API Gateway
- Zipkin
- Cassandra

## Variables

The following table contains the variables that are used by the ```docker-compose.yml``` file.
Those without a default value must be set using the ```export``` command.


| Variable                              | Description                                       | Default value         |
|:--------------------------------------|:--------------------------------------------------|:---------------------:|
| API_GATEWAY_VERSION                   | The API Gateway Docker image tag                  | -                     |
| USERS_SERVICE_VERSION                 | The Users Service Docker image tag                | -                     |
| USERS_SERVICE_POSTGRES_USER           | The Users Service database username               | users-service         |
| USERS_SERVICE_POSTGRES_PASSWORD       | The Users Service database user's password        | users-service         |
| USERS_SERVICE_POSTGRES_DATABASE       | The Users Service database name                   | users-service         |
| USERS_SERVICE_FIRST_USER_USERNAME     | The username of the first admin user              | administrator         |
| USERS_SERVICE_FIRST_USER_PASSWORD     | The password of the first admin user              | Cep1234!              |
| LTI_SERVICE_VERSION                   | The LTI Service Docker image tag                  | -                     |
| LTI_SERVICE_POSTGRES_USER             | The LTI Service database username                 | lti-service           |
| LTI_SERVICE_POSTGRES_PASSWORD         | The LTI Service database user's password          | lti-service           |
| LTI_SERVICE_POSTGRES_DATABASE         | The LTI Service database name                     | lti-service           |
| LTI_APP_VERSION                       | The LTI App Docker image tag                      | -                     |
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

## Exposed services

The following services are exposed to the outside world and can be accessed from the host machine.

| Service                               | Port  |
|:--------------------------------------|:------|
| API Gateway                           | 8000  |
| LTI App                               | 5000  |
| Service Registry                      | 8761  |
| Zipkin                                | 9411  |
| Playground Service Postgres           | 15432 |
| Evaluations Service Postgres          | 25432 |
| Users Service Postgres                | 35432 |
| LTI Service Postgres                  | 45432 |


For example, to query traces, just access from your favorite browser to http://localhost:9411. You will see the Zipkin UI.
