# Playground and Executor Services

Stack that allows running the [Playground Service](https://github.com/coding-eval-platform/playground-service) together with the [Executor Service](https://github.com/coding-eval-platform/executor-service), using Kafka to communicate between themselves.

## Components

- Apache Zookeeper
- Apache Kafka
- PostgreSQL database
- Playground Service
- Nginx reverse proxy

## Variables

The following table contains the variables that are used by the ```docker-compose.yml``` file.
Those without a default value must be set using the ```export``` command.


| Variable                              | Description                                       | Default value         |
|:--------------------------------------|:--------------------------------------------------|:---------------------:|
| PLAYGROUND_SERVICE_VERSION            | The Playground Service Docker image tag           | 0.0.1-RELEASE         |
| PLAYGROUND_SERVICE_POSTGRES_USER      | The Playground Service database username          | playground-service    |
| PLAYGROUND_SERVICE_POSTGRES_PASSWORD  | The Playground Service database user's password   | playground-service    |
| PLAYGROUND_SERVICE_POSTGRES_DATABASE  | The Playground Service database name              | playground-service    |
| EXECUTOR_SERVICE_VERSION              | The Executor Service Docker image tag             | 0.0.1-RELEASE         |


## Example

The following is a full example that indicates how to run the stack.

```
$ docker-compose up
```
