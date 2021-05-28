# Amazon Linux 2 - Docker in Docker (dind)

[Amazon Linux 2](https://aws.amazon.com/amazon-linux-2/) container image with [systemd](https://systemd.io) and [Docker Engine](https://www.docker.com/products/container-runtime).

## Registries

The image is available on following registries:

- [Docker Hub](https://hub.docker.com/repository/docker/nikovirtala/amazonlinux-dind)
- [Amazon ECR Public Gallery](https://gallery.ecr.aws/nikovirtala/amazonlinux-dind)
- [GitHub Packages](https://github.com/users/nikovirtala/packages/container/package/amazonlinux-dind)

## Usage

### Build container image

```sh
docker build -t amazonlinux-dind:latest .
```

### Create the container and run it on background (local build)

```sh
docker run -d --name amazonlinux-dind \
  --privileged \
  -v /sys/fs/cgroup:/sys/fs/cgroup:ro \
  amazonlinux-dind:latest
```

### Create the container and run it on background (Docker Hub)

```sh
docker run -d --name amazonlinux-dind \
  --privileged \
  -v /sys/fs/cgroup:/sys/fs/cgroup:ro \
  nikovirtala/amazonlinux-dind:latest
```

### Create the container and run it on background (Amazon ECR Public Gallery)

```sh
docker run -d --name amazonlinux-dind \
  --privileged \
  -v /sys/fs/cgroup:/sys/fs/cgroup:ro \
  public.ecr.aws/nikovirtala/amazonlinux-dind:latest
```

### Create the container and run it on background (GitHub Packages)

```sh
docker run -d --name amazonlinux-dind \
  --privileged \
  -v /sys/fs/cgroup:/sys/fs/cgroup:ro \
  ghcr.io/nikovirtala/amazonlinux-dind:latest
```

### Enter to the container

```sh
docker exec -it amazonlinux-dind /bin/bash
```

### Stop the container

```sh
docker stop amazonlinux-dind
```

### Start the container

```sh
docker start amazonlinux-dind
```

### Remove the container

```sh
docker rm -f amazonlinux-dind
```
