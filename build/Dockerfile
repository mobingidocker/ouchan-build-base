FROM linuxbrew/brew:2.4.5

MAINTAINER Alphaus <dev@mobingi.com>

RUN SDK=google-cloud-sdk-307.0.0-linux-x86_64.tar.gz \
    && curl -LO https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/$SDK && tar xzf $SDK \
    && ./google-cloud-sdk/install.sh --quiet && rm $SDK \
    && ./google-cloud-sdk/bin/gcloud components install kubectl \
    && curl -s https://dl.google.com/go/go1.14.4.linux-amd64.tar.gz | tar -v -C /usr/local -xz \
    && mkdir -p /go/src /go/bin \
    && apt-get update && apt-get install -y python3-pip gcc wget unzip \
    && pip3 install --user --upgrade awscli \
    && brew tap aws/tap && brew install aws-sam-cli \
    && TRFM=terraform_0.13.1_linux_amd64.zip && wget https://releases.hashicorp.com/terraform/0.13.1/$TRFM \
    && unzip $TRFM && mv terraform /usr/local/bin/ && rm $TRFM

ENV GOPATH /go
ENV GOROOT /usr/local/go
ENV PATH /usr/local/go/bin:/go/bin:/usr/local/bin:/home/linuxbrew/google-cloud-sdk/bin:/root/.local/bin:$PATH

CMD ["bash"]
