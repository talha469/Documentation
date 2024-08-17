![Alt text](https://upload.wikimedia.org/wikipedia/commons/e/ea/Docker_%28container_engine%29_logo_%28cropped%29.png)

# Docker Image Upload Guide

## Overview

This guide provides step-by-step instructions for uploading a Docker image to Docker Hub. Docker Hub is a cloud-based registry that allows you to store and share Docker images.

## Prerequisites

- Docker installed on your local machine.
- A Docker Hub account.

## Steps

### 1. Tag Your Docker Image

Before uploading your Docker image, you need to tag it with your Docker Hub repository name. Use the following command:

```bash
docker tag <your_image_name>:version <your_dockerhub_username>/<your_repository_name>:<your_tag>
```
Replace the placeholders:

`<your_image_name>:` The name of your local Docker image.

`<your_dockerhub_username>:` Your Docker Hub username.

`<your_repository_name>:` The name of the repository on Docker Hub where you want to upload the image.

`<your_tag>:` A tag for your image (e.g., latest or v1.0).


### 2. Login to Docker

```sh
docker login
```

### 3. push your image to docker hub

```sh
docker push <your_dockerhub_username>/<your_repository_name>:<your_tag>
```

### 4. verify
```sh
docker search <your_dockerhub_username>/<your_repository_name>
```
