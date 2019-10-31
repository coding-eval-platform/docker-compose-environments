# Infrastructure

Stack that allows running the infrastructure needed by the LTI service and app to operate.

## Components

- Apache Zookeeper
- Apache Kafka
- PostgreSQL database
- Service Registry
- Evaluations Service
- Users Service
- API Gateway

## Variables

The following table contains the variables that are used by the ```docker-compose.yml``` file.
Those without a default value must be set using the ```export``` command.


| Variable                              | Description                                       | Default value                             |
|:--------------------------------------|:--------------------------------------------------|:-----------------------------------------:|
| API_GATEWAY_VERSION                   | The API Gateway Docker image tag                  | -                                         |
| USERS_SERVICE_POSTGRES_USER           | The Users Service database username               | coding-eval-platform__users-service       |
| USERS_SERVICE_POSTGRES_PASSWORD       | The Users Service database user's password        | coding-eval-platform__users-service       |
| USERS_SERVICE_POSTGRES_DATABASE       | The Users Service database name                   | coding-eval-platform__users-service       |
| EVALUATIONS_SERVICE_POSTGRES_USER     | The Evaluations Service database username         | coding-eval-platform__evaluations-service |
| EVALUATIONS_SERVICE_POSTGRES_PASSWORD | The Evaluations Service database user's password  | coding-eval-platform__evaluations-service |
| EVALUATIONS_SERVICE_POSTGRES_DATABASE | The Evaluations Service database name             | coding-eval-platform__evaluations-service |
| PLAYGROUND_SERVICE_POSTGRES_USER      | The Playground Service database username          | coding-eval-platform__playground-service  |
| PLAYGROUND_SERVICE_POSTGRES_PASSWORD  | The Playground Service database user's password   | coding-eval-platform__playground-service  |
| PLAYGROUND_SERVICE_POSTGRES_DATABASE  | The Playground Service database name              | coding-eval-platform__playground-service  |
| SERVICE_REGISTRY_VERSION              | The Service Registry Docker image tag             | -                                         |
| USERS_SERVICE_VERSION                 | The Users Service Docker image tag                | -                                         |
| USERS_SERVICE_FIRST_USER_USERNAME     | The username of the first admin user              | administrator                             |
| USERS_SERVICE_FIRST_USER_PASSWORD     | The password of the first admin user              | Cep1234!                                  |
| EVALUATIONS_SERVICE_VERSION           | The Evaluations Service Docker image tag          | -                                         |


**Note:** In fact, there are default values for all the Docker images, but they are snapshot builds.


## Example

The following is a full example that indicates how to run the stack.

```
$ export API_GATEWAY_VERSION=...
$ docker-compose up
```
