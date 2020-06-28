FROM google/cloud-sdk:298.0.0-slim

MAINTAINER Alphaus <dev@mobingi.com>

USER root

RUN curl -s https://dl.google.com/go/go1.14.4.linux-amd64.tar.gz | tar -v -C /usr/local -xz \
    && mkdir -p /go/src /go/bin \
    && apt-get install kubectl

ENV GOPATH /go
ENV GOROOT /usr/local/go
ENV PATH /usr/local/go/bin:/go/bin:/usr/local/bin:$PATH

CMD ["bash"]
