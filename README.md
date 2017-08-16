# gcloud-sdk-docker
Image that inherits from google/cloud-sdk, and installs docker into it.

**Why?** Because we need this image to run `gcloud` *and* `docker`.

## Usage

```
docker run -v /var/run/docker.sock:/var/run/docker.sock devsu/gcloud-sdk-docker
```

Using docker compose:

```
version: '3'
services:
    gcloud:
        image: devsu/gcloud-sdk-docker
        volumes:
        - '/var/run/docker.sock:/var/run/docker.sock'
```

## License and Credits

Copyright 2017, by the [Docker Experts](https://devsu.com) at Devsu

MIT License