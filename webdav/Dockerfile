FROM debian:9


RUN apt update && apt install -y wget && \
    mkdir -p /webdav && \
    mkdir -p /webdav/data && \
    cd /webdav && \
    wget https://github.com/hacdias/webdav/releases/download/v1.2.0/linux-amd64-webdav.tar.gz && \
    tar xzvf linux-amd64-webdav.tar.gz && \
    rm -rf linux-amd64-webdav.tar.gz

WORKDIR /webdav

CMD ["/webdav/webdav"]
