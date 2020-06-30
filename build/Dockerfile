FROM linuxbrew/brew:2.4.2

MAINTAINER Alphaus <dev@mobingi.com>

RUN SDK=google-cloud-sdk-298.0.0-linux-x86_64.tar.gz \
    && curl -LO https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/$SDK && tar xzf $SDK \
    && ./google-cloud-sdk/install.sh --quiet && rm $SDK \
    && ./google-cloud-sdk/bin/gcloud components install kubectl \
    && curl -s https://dl.google.com/go/go1.14.4.linux-amd64.tar.gz | tar -v -C /usr/local -xz \
    && mkdir -p /go/src /go/bin \
    && apt-get update && apt-get install -y python3-pip gcc \
    && pip3 install --user --upgrade awscli \
    && brew tap aws/tap && brew install aws-sam-cli

ENV GOPATH /go
ENV GOROOT /usr/local/go
ENV PATH /usr/local/go/bin:/go/bin:/usr/local/bin:/home/linuxbrew/google-cloud-sdk/bin:/root/.local/bin:$PATH

CMD ["bash"]
