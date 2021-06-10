# rabbitmq-exporter

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/rabbitmq-exporter) [![Testing Build](https://github.com/rolehippie/rabbitmq-exporter/workflows/testing/badge.svg)](https://github.com/rolehippie/rabbitmq-exporter/actions?query=workflow%3Atesting) [![Readme Build](https://github.com/rolehippie/rabbitmq-exporter/workflows/readme/badge.svg)](https://github.com/rolehippie/rabbitmq-exporter/actions?query=workflow%3Areadme) [![Galaxy Build](https://github.com/rolehippie/rabbitmq-exporter/workflows/galaxy/badge.svg)](https://github.com/rolehippie/rabbitmq-exporter/actions?query=workflow%3Agalaxy) [![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/rabbitmq-exporter)](https://github.com/rolehippie/rabbitmq-exporter/blob/master/LICENSE) 

Ansible role to install and configure a Prometheus exporter for RabbitMQ. 

## Sponsor 

[![Proact Deutschland GmbH](https://proact.eu/wp-content/uploads/2020/03/proact-logo.png)](https://proact.eu) 

Building and improving this Ansible role have been sponsored by my employer **Proact Deutschland GmbH**.

## Table of content

* [Default Variables](#default-variables)
  * [rabbitmq_exporter_capabilities](#rabbitmq_exporter_capabilities)
  * [rabbitmq_exporter_exporters](#rabbitmq_exporter_exporters)
  * [rabbitmq_exporter_image](#rabbitmq_exporter_image)
  * [rabbitmq_exporter_network](#rabbitmq_exporter_network)
  * [rabbitmq_exporter_password](#rabbitmq_exporter_password)
  * [rabbitmq_exporter_publish](#rabbitmq_exporter_publish)
  * [rabbitmq_exporter_url](#rabbitmq_exporter_url)
  * [rabbitmq_exporter_username](#rabbitmq_exporter_username)
  * [rabbitmq_exporter_version](#rabbitmq_exporter_version)
* [Dependencies](#dependencies)
* [License](#license)
* [Author](#author)

---

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
rabbitmq_exporter_version: v1.0.0-RC7.1
```

## Dependencies

* [rolehippie.docker](https://github.com/rolehippie/docker)

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
