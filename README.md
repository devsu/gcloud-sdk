# gcloud-sdk-docker
Image that inherits from google/cloud-sdk, and installs required libraries to run siblings dockers.

## Why?

Because we need this image to run `gcloud` *and* `docker`, but when using the official gcloud image and running docker, it produces this error:

```
docker: error while loading shared libraries: libltdl.so.7: cannot open shared object file: No such file or directory
```

## Usage

```
docker run -it -v /var/run/docker.sock:/var/run/docker.sock $(which docker):/usr/bin/docker devsu/gcloud-sdk-docker:alpine
```

Only alpine variant is available (for now).

## License and Credits

Copyright 2017, by the [Docker Experts](https://devsu.com) at Devsu

MIT License