FROM circleci/php:7.1.15-apache-jessie-node-browsers

MAINTAINER Mobingi <dev@mobingi.com>

RUN apt-get update && apt-get install --no-install-recommends -y \
    ca-certificates \
    curl \
    mercurial \
    git-core

RUN curl -s https://dl.google.com/go/go1.10.3.linux-amd64.tar.gz | tar -v -C /usr/local -xz

ENV GOPATH /go
ENV GOROOT /usr/local/go
ENV PATH /usr/local/go/bin:/go/bin:/usr/local/bin:$PATH

CMD ["bash"]
