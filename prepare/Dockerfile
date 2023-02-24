FROM linuxbrew/brew:latest

MAINTAINER Alphaus <dev@mobingi.com>

RUN curl -s https://dl.google.com/go/go1.19.6.linux-amd64.tar.gz | tar -v -C /usr/local -xz \
    && mkdir -p /go/src /go/bin \
    && apt-get update && apt-get install -y gcc

ENV GOPATH /go
ENV GOROOT /usr/local/go
ENV PATH /usr/local/go/bin:/go/bin:/usr/local/bin:/home/linuxbrew/google-cloud-sdk/bin:/root/.local/bin:$PATH

CMD ["bash"]
