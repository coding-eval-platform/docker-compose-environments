# Docker Compose Stacks

Repository containing several stacks created with Docker Compose, mainly used for development and testing purposes.

## Getting started

The following sections will explain the basic stuff for using these stacks.

### Prerequisites / Needed Software

All the stacks included in this project are created using [Docker Compose](https://docs.docker.com/compose/), which relies on the [Docker Engine](https://docs.docker.com/engine/).

So, briefly, what you need is:
- The Docker Engine
- Docker Compose

#### Installation guide for MacOS

Docker Desktop for Mac is an easy-to-install desktop app that allows using Docker in MacOS. This app contains both the Docker Engine, and Docker Compose, together with other Docker tools.

You can find useful information in the following links:

- [DockerHub](https://hub.docker.com/editions/community/docker-ce-desktop-mac)
- [Official Docs](https://docs.docker.com/docker-for-mac/)
- [How to install Docker Desktop for Mac?](https://docs.docker.com/docker-for-mac/install/)

Also, you can install it from the command line. If you have homebrew, just type:

```
$ brew cask install docker 
```


### How to use them?

The ```stacks``` directory contains the stacks that are created. Each of them is a directory, which in turn contain

The ```stacks``` directory contains a subdirectory for each stack created within this project. Those stacks subdirectories will contain a ```docker-compose.yml``` file where all the stack configuration is declared. Also, some might contain a ```.env``` file declaring default values. Each stack will contain a ```README.md``` file with information about it (also indicating mandatory and overridable values).

To start a stack just ```cd``` into the said stack subdirectory, and run Docker compose, exporting the needed variables.

For example, to run the ```evaluations-service-standalone``` stack, execute the following commands:

```
$ cd stacks/evaluations-service-standalone/
$ export EVALUATIONS_SERVICE_VERSION=0.0.2-RELEASE
$ docker-compose up
```

If you want to rename a variable defined in the ```.env``` just export it. For example:

```
$ export POSTGRES_USER=another-user
```

Note that this won't override the ```.env``` file.


## License

Copyright 2019 Bellini & Lobo

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.


## Authors

* [Juan Marcos Bellini](https://github.com/juanmbellini)
* [Daniel Lobo](https://github.com/lobo)
