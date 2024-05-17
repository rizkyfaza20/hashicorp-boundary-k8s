# Boundary & Vault Helm Chart

## Overview

This repository contain of Hashicorp Vault and Boundary self-hosted which created on Helm charts and also Docker Compose script to run. Created for learning and testing purposes only.

For the Helm Chart, still WIP. But you can test the Docker Compose for test out the infrastructure of Boundary.

## Prerequisites

- **Helm 3.6+**
- **Kubernetes 1.22+**
- **Docker and Docker Compose**

## Installation for Vault

To install the latest version of this chart, add the Hashicorp helm repository and run `helm install`:

```console
$ helm repo add hashicorp https://helm.releases.hashicorp.com
"hashicorp" has been added to your repositories

$ helm install vault hashicorp/vault
```

For detailed installation instructions and configuration options, refer to the [Vault Helm Chart documentation](https://developer.hashicorp.com/vault/docs/platform/k8s/helm).

## Configuration

The `values.yaml` file contains numerous options for configuring Vault. These options are fully documented on the [Vault website](https://developer.hashicorp.com/vault/docs/platform/k8s/helm).


### Running Tests Using Docker

Inside the docker-compose.yaml, contains of service:
- Boundary
- DB Initialization (Postgres)
- Postgresql
- Busybox (Health Check)

```
docker compose up -d # run the script detached mode
```


## License

This project is under the Mozilla Public License 2.0. For more details, see the [LICENSE](argocd/vault/LICENSE) file.

## Additional Resources

- [Vault and Kubernetes documentation](https://developer.hashicorp.com/vault/docs/platform/k8s)
- [Vault Helm Chart Values](https://developer.hashicorp.com/vault/docs/platform/k8s/helm)

