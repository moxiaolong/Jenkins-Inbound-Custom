FROM jenkins/inbound-agent:jdk17
USER root
RUN pwd
RUN curl -O https://dl.google.com/go/go1.20.2.linux-amd64.tar.gz
RUN tar -xzf go1.20.2.linux-amd64.tar.gz
RUN rm -f go1.20.2.linux-amd64.tar.gz
ENV PATH="/home/jenkins/go/bin:${PATH}"
RUN go version
RUN curl -O https://download.docker.com/linux/static/stable/x86_64/docker-23.0.1.tgz
RUN tar -xzf docker-23.0.1.tgz
RUN rm -f docker-23.0.1.tgz
RUN mv docker/* /usr/bin/
ADD ./daemon.json /etc/docker/
ADD ./docker.service /etc/systemd/system/
RUN chmod +x /etc/systemd/system/docker.service
RUN docker -v

RUN sleep 10000000