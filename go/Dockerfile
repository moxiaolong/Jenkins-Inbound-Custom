FROM jenkins/inbound-agent:jdk17
USER root
RUN pwd
RUN curl -O https://dl.google.com/go/go1.20.2.linux-amd64.tar.gz
RUN tar -xzf go1.20.2.linux-amd64.tar.gz
ENV PATH="/home/jenkins/go/bin:${PATH}"
RUN go version