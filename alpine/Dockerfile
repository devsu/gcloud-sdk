FROM google/cloud-sdk:alpine

RUN echo 'http://dl-cdn.alpinelinux.org/alpine/edge/community' >> /etc/apk/repositories \
  && apk --no-cache add docker py-pip \
  && pip install docker-compose

WORKDIR /root