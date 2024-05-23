# Contributing

## Developing

Please refer to
the [rockcraft](https://canonical-craft-parts.readthedocs-hosted.com/en/latest/reference/index.html)
documentations to learn how to develop a rock.

Please install `pre-commit` hooks to help enforce various validations:

```shell
pre-commit install -t commit-msg
```

## Building and Running Locally

You can build the rock using the following command:

```shell
rockcraft pack -v
```

Assuming the [`skopeo`](https://snapcraft.io/install/skopeo/ubuntu) has been
installed. Import the created rock into Docker:

```shell
sudo /snap/rockcraft/current/bin/skopeo --insecure-policy copy oci-archive:<local-rock-name>.rock docker-daemon:oathkeeper:latest
```

Run an Oathkeeper container using Docker:

```shell
docker run -d \
  --rm \
  --name <container-name> \
  oathkeeper:latest
```
