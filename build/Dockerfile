FROM homebrew/brew:4.6.20
RUN SDK=google-cloud-sdk-549.0.1-linux-x86_64.tar.gz; \
    curl -LO https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/$SDK && tar xzf $SDK \
    && ./google-cloud-sdk/install.sh --quiet && rm $SDK \
    && ./google-cloud-sdk/bin/gcloud components install kubectl \
    && curl -s https://dl.google.com/go/go1.25.5.linux-amd64.tar.gz | sudo tar -v -C /usr/local -xz && mkdir -p /home/linuxbrew/go/ \
    && sudo apt-get update && sudo apt-get install -y python3-pip gcc wget \
    && pip3 install --user --upgrade awscli \
    && brew tap aws/tap && brew install aws-sam-cli
ENV GOPATH=/home/linuxbrew/go
ENV GOROOT=/usr/local/go
ENV PATH=/home/linuxbrew/.local/bin:/home/linuxbrew/.linuxbrew/opt/python@3.7/bin:/usr/local/go/bin:/home/linuxbrew/go/bin:/usr/local/bin:/home/linuxbrew/google-cloud-sdk/bin:$PATH
RUN echo "$HOME" && brew --version && python3 --version && aws --version && sam --version
CMD ["bash"]
