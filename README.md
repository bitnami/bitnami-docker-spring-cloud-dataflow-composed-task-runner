
# What is Spring Cloud Data Flow Composed Task Runner?

> The Composed Task Runner is used by the Data Flow server to parse a directed graph DSL, execute a REST-ful call against a specified instance, launch the associated task definition, and check the status of the task. Following this, the Composed Task Runner will either proceed to the next task in the graph or fail based on the DSL configuration.

[See how to deploy Spring Cloud Data Flow Server](https://github.com/bitnami/bitnami-docker-spring-cloud-dataflow)

# TL;DR

```console
$ docker run --name spring-cloud-dataflow-composed-task-runner bitnami/spring-cloud-dataflow-composed-task-runner:latest
```

# Why use Bitnami Images?

* Bitnami closely tracks upstream source changes and promptly publishes new versions of this image using our automated systems.
* With Bitnami images the latest bug fixes and features are available as soon as possible.
* Bitnami containers, virtual machines and cloud images use the same components and configuration approach - making it easy to switch between formats based on your project needs.
* All our images are based on [minideb](https://github.com/bitnami/minideb) a minimalist Debian based container image which gives you a small base container image and the familiarity of a leading Linux distribution.
* All Bitnami images available in Docker Hub are signed with [Docker Content Trust (DCT)](https://docs.docker.com/engine/security/trust/content_trust/). You can use `DOCKER_CONTENT_TRUST=1` to verify the integrity of the images.
* Bitnami container images are released daily with the latest distribution packages available.


> This [CVE scan report](https://quay.io/repository/bitnami/spring-cloud-dataflow-composed-task-runner?tab=tags) contains a security report with all open CVEs. To get the list of actionable security issues, find the "latest" tag, click the vulnerability report link under the corresponding "Security scan" field and then select the "Only show fixable" filter on the next page.

# Supported tags and respective `Dockerfile` links

Learn more about the Bitnami tagging policy and the difference between rolling tags and immutable tags [in our documentation page](https://docs.bitnami.com/tutorials/understand-rolling-tags-containers/).


* [`2`, `2-debian-10`, `2.7.0`, `2.7.0-debian-10-r32`, `latest` (2/debian-10/Dockerfile)](https://github.com/bitnami/bitnami-docker-spring-cloud-dataflow-composed-task-runner/blob/2.7.0-debian-10-r32/2/debian-10/Dockerfile)

Subscribe to project updates by watching the [bitnami/spring-cloud-dataflow-composed-task-runner GitHub repo](https://github.com/bitnami/bitnami-docker-spring-cloud-dataflow-composed-task-runner).

# Get this image

The recommended way to get the Bitnami spring-cloud-dataflow-composed-task-runner Docker Image is to pull the prebuilt image from the [Docker Hub Registry](https://hub.docker.com/r/bitnami/spring-cloud-dataflow-composed-task-runner).

```console
$ docker pull bitnami/spring-cloud-dataflow-composed-task-runner:latest
```

To use a specific version, you can pull a versioned tag. You can view the [list of available versions](https://hub.docker.com/r/bitnami/spring-cloud-dataflow-composed-task-runner/tags/) in the Docker Hub Registry.

```console
$ docker pull bitnami/spring-cloud-dataflow-composed-task-runner:[TAG]
```

If you wish, you can also build the image yourself.

```console
$ docker build -t bitnami/spring-cloud-dataflow-composed-task-runner:latest 'https://github.com/bitnami/bitnami-docker-spring-cloud-dataflow-composed-task-runner.git#master:2/debian-10'
```

# Configuration

## Running commands

To run tasks inside this container you can use `docker run`:

```console
$ docker run --rm --name spring-cloud-dataflow-composed-task-runner bitnami/spring-cloud-dataflow-composed-task-runner:latest <runner_args>
```

# Contributing

We'd love for you to contribute to this container. You can request new features by creating an [issue](https://github.com/bitnami/bitnami-docker-spring-cloud-dataflow-composed-task-runner/issues), or submit a [pull request](https://github.com/bitnami/bitnami-docker-spring-cloud-dataflow-composed-task-runner/pulls) with your contribution.

# Issues

If you encountered a problem running this container, you can file an [issue](https://github.com/bitnami/bitnami-docker-spring-cloud-dataflow-composed-task-runner/issues/new). For us to provide better support, be sure to include the following information in your issue:

- Host OS and version
- Docker version (`docker version`)
- Output of `docker info`
- Version of this container
- The command you used to run the container, and any relevant output you saw (masking any sensitive information)

# License

Copyright 2021 Bitnami

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
