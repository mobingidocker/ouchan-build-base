FROM homebrew/brew:4.6.20
RUN curl -s https://dl.google.com/go/go1.25.5.linux-amd64.tar.gz | sudo tar -v -C /usr/local -xz \
    && sudo mkdir -p /go/src /go/bin \
    && sudo apt-get update && sudo apt-get install -y gcc && mkdir $HOME/go/
ENV GOPATH=$HOME/go
ENV GOROOT=/usr/local/go
ENV PATH=/usr/local/go/bin:/go/bin:/usr/local/bin:/home/linuxbrew/google-cloud-sdk/bin:/root/.local/bin:$PATH
RUN env
CMD ["bash"]
