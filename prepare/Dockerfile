FROM homebrew/brew:4.6.20
RUN curl -s https://dl.google.com/go/go1.25.6.linux-amd64.tar.gz | sudo tar -v -C /usr/local -xz \
    && sudo apt-get update && sudo apt-get install -y gcc && mkdir -p /home/linuxbrew/go/
ENV GOPATH=/home/linuxbrew/go
ENV GOROOT=/usr/local/go
ENV PATH=/home/linuxbrew/.local/bin:/usr/local/go/bin:/home/linuxbrew/go/bin:/usr/local/bin:$PATH
CMD ["bash"]
