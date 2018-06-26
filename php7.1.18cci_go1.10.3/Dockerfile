FROM circleci/php:7.1.15-apache-jessie-node-browsers

MAINTAINER Mobingi <dev@mobingi.com>

USER root

RUN curl -s https://dl.google.com/go/go1.10.3.linux-amd64.tar.gz | tar -v -C /usr/local -xz \
    && mkdir -p /go/src /go/bin \
    && chown -R circleci:circleci /go

USER circleci

ENV GOPATH /go
ENV GOROOT /usr/local/go
ENV PATH /usr/local/go/bin:/go/bin:/usr/local/bin:$PATH

CMD ["bash"]
