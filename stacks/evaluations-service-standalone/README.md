# Evaluations Service Standalone

Stack that allows running the [Evaluations Service](https://github.com/coding-eval-platform/evaluations-service) in a standalone mode.

## Components

- PostgreSQL database
- Evaluations Service
- Nginx reverse proxy

## Variables

The following table contains the variables that are used by the ```docker-compose.yml``` file.
Those without a default value must be set using the ```export``` command.


| Variable                      | Description                               | Default value         |
|:------------------------------|:------------------------------------------|:---------------------:|
| EVALUATIONS_SERVICE_VERSION   | The Evaluations Service Docker image tag  | -                     |
| POSTGRES_USER                 | The database username                     | evaluations-service   |
| POSTGRES_PASSWORD             | The database user's password              | evaluations-service   |
| POSTGRES_DATABASE             | The database name                         | evaluations-service   |


## Example

The following is a full example that indicates how to run the stack.

```
$ export EVALUATIONS_SERVICE_VERSION=0.0.2-RELEASE
$ docker-compose up
```