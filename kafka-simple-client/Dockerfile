FROM adoptopenjdk/maven-openjdk11

RUN apt-get update -y && \
    apt-get install -y git ca-certificates

WORKDIR /opt/
RUN git clone --single-branch --branch 5.5.1-post https://github.com/confluentinc/examples.git

WORKDIR /opt/examples/clients/cloud/java
RUN mvn clean package

