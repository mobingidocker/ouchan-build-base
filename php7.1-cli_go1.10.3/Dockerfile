FROM php:7.1-cli

MAINTAINER Mobingi <dev@mobingi.com>

RUN curl -s https://dl.google.com/go/go1.10.3.linux-amd64.tar.gz | tar -v -C /usr/local -xz

ENV GOPATH /go
ENV GOROOT /usr/local/go
ENV PATH /usr/local/go/bin:/go/bin:/usr/local/bin:$PATH

CMD ["bash"]
