FROM ubuntu:latest
RUN apt-get update && \
    apt-get install -y  curl  wget &&\
    apt-get clean && rm -rf /var/lib/apt/lists/*

ENV HUGO_VERSION=0.138.0
RUN wget -O HUGO.deb https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_${HUGO_VERSION}_linux-amd64.deb && \
    dpkg -i HUGO.deb &&\
    rm -r HUGO.deb
RUN hugo version

CMD ["/bin/bash"]