# Infrastructure

Stack that allows running the infrastructure of the platform, in order to generate an environment to run the services in standalone mode.

## Components

- Apache Zookeeper
- Apache Kafka
- PostgreSQL database
- Service Registry
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
| LTI_SERVICE_POSTGRES_USER             | The LTI Service database username                 | coding-eval-platform__lti-service         |
| LTI_SERVICE_POSTGRES_PASSWORD         | The LTI Service database user's password          | coding-eval-platform__lti-service         |
| LTI_SERVICE_POSTGRES_DATABASE         | The LTI Service database name                     | coding-eval-platform__lti-service         |
| SERVICE_REGISTRY_VERSION              | The Service Registry Docker image tag             | -                                         |


**Note:** In fact, there are default values for all the Docker images, but they are snapshot builds.


## Example

The following is a full example that indicates how to run the stack.

```
$ export API_GATEWAY_VERSION=...
$ docker-compose up
```
