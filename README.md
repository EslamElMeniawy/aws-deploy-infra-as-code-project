# `aws-deploy-infra-as-code-project`

> `AWS` deploy infrastructure as code project for `DevOps` course

## Content

- [`InfrastructureDiagram.svg`](InfrastructureDiagram.svg) - Contains the diagram for the solution.
- [`network.yml`](network.yml) and [`network-parameters.json`](network-parameters.json) - Used for creating network infrastructure.
- [`udagram.yml`](udagram.yml) and [`udagram-parameters.json`](udagram-parameters.json) - Used for creating `Udagram` infrastructure.
- [`run.sh`](run.sh) - Helper script for automating spin-up and tear-down of the infrastructure.

## Using [`run.sh`](run.sh) Instructions

The [`run.sh`](run.sh) script is used for creating and deleting the infrastructure.

### Creation

To create the network infrastructure use below command:

```sh
./run.sh deploy us-east-1 udagram-network-stack network.yml network-parameters.json
```

To create the `Udagram` infrastructure use below command:

```sh
./run.sh deploy us-east-1 udagram-stack udagram.yml udagram-parameters.json
```

### Deletion

To delete the `Udagram` infrastructure use below command:

```sh
./run.sh delete us-east-1 udagram-stack
```

To delete the network infrastructure use below command:

```sh
./run.sh delete us-east-1 udagram-network-stack
```

## Working Test

Use below URL for verifying that the solution works.

> [http://udagra-loadb-66o7lrzuv5uj-914457817.us-east-1.elb.amazonaws.com/](http://udagra-loadb-66o7lrzuv5uj-914457817.us-east-1.elb.amazonaws.com/).
