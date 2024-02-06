# rabbitmq-exporter

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/rabbitmq-exporter)
[![General Workflow](https://github.com/rolehippie/rabbitmq-exporter/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/rabbitmq-exporter/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/rabbitmq-exporter/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/rabbitmq-exporter/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/rabbitmq-exporter/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/rabbitmq-exporter/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/rabbitmq-exporter)](https://github.com/rolehippie/rabbitmq-exporter/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.rabbitmq__exporter-blue)](https://galaxy.ansible.com/rolehippie/rabbitmq_exporter)

Ansible role to install and configure a Prometheus exporter for RabbitMQ.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [rabbitmq_exporter_capabilities](#rabbitmq_exporter_capabilities)
  - [rabbitmq_exporter_exporters](#rabbitmq_exporter_exporters)
  - [rabbitmq_exporter_image](#rabbitmq_exporter_image)
  - [rabbitmq_exporter_network](#rabbitmq_exporter_network)
  - [rabbitmq_exporter_password](#rabbitmq_exporter_password)
  - [rabbitmq_exporter_publish](#rabbitmq_exporter_publish)
  - [rabbitmq_exporter_pull_image](#rabbitmq_exporter_pull_image)
  - [rabbitmq_exporter_url](#rabbitmq_exporter_url)
  - [rabbitmq_exporter_username](#rabbitmq_exporter_username)
  - [rabbitmq_exporter_version](#rabbitmq_exporter_version)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

## Default Variables

### rabbitmq_exporter_capabilities

List of capabilities

#### Default value

```YAML
rabbitmq_exporter_capabilities:
  - bert
  - no_sort
```

### rabbitmq_exporter_exporters

List of enabled exporters

#### Default value

```YAML
rabbitmq_exporter_exporters:
  - connections
  - shovel
  - federation
  - exchange
  - node
  - queue
```

### rabbitmq_exporter_image

Docker image to use and run

#### Default value

```YAML
rabbitmq_exporter_image: kbudde/rabbitmq-exporter:{{ rabbitmq_exporter_version }}
```

### rabbitmq_exporter_network

A Docker network to assign the container

#### Default value

```YAML
rabbitmq_exporter_network:
```

### rabbitmq_exporter_password

Password to access RabbitMQ

#### Default value

```YAML
rabbitmq_exporter_password: guest
```

### rabbitmq_exporter_publish

Publish the Docker image on thet binding

#### Default value

```YAML
rabbitmq_exporter_publish: 9419
```

### rabbitmq_exporter_pull_image

Pull image as part of the tasks

#### Default value

```YAML
rabbitmq_exporter_pull_image: true
```

### rabbitmq_exporter_url

URL to access RabbitMQ

#### Default value

```YAML
rabbitmq_exporter_url: http://127.0.0.1:15672
```

### rabbitmq_exporter_username

Username to access RabbitMQ

#### Default value

```YAML
rabbitmq_exporter_username: guest
```

### rabbitmq_exporter_version

Version of the Docker image

#### Default value

```YAML
rabbitmq_exporter_version: 1.0.0-RC19
```

## Discovered Tags

**_rabbitmq-exporter_**


## Dependencies

- [rolehippie.docker](https://github.com/rolehippie/docker)
- [community.docker](https://github.com/ansible-collections/community.docker)

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
