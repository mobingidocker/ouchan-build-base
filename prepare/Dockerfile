FROM homebrew/brew:4.6.20
RUN curl -s https://dl.google.com/go/go1.21.0.linux-amd64.tar.gz | sudo tar -v -C /usr/local -xz \
    && sudo mkdir -p /go/src /go/bin \
    && sudo apt-get update && sudo apt-get install -y gcc
ENV GOPATH /go
ENV GOROOT /usr/local/go
ENV PATH /usr/local/go/bin:/go/bin:/usr/local/bin:/home/linuxbrew/google-cloud-sdk/bin:/root/.local/bin:$PATH
CMD ["bash"]
