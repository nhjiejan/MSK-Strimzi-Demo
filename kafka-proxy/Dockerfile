FROM adoptopenjdk/openjdk11:jdk-11.0.8_10-ubuntu-slim
ENV VERSION=v0.2.5

RUN apt-get update && apt-get -y install curl tar

WORKDIR /usr/local/bin/

# instakk kafka-proxy
RUN curl -Ls https://github.com/grepplabs/kafka-proxy/releases/download/${VERSION}/kafka-proxy-${VERSION}-linux-amd64.tar.gz | tar xz && \
    rm -f https://github.com/grepplabs/kafka-proxy/releases/download/${VERSION}/kafka-proxy-${VERSION}-linux-amd64.tar.gz

# Clean up
RUN apt-get -y clean && \
    apt-get -y autoremove --purge

CMD ["/usr/local/bin/kafka-proxy"]
