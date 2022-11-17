FROM jenkins/jenkins:latest-jdk11

USER root

RUN apt-get update -y \
    && apt-get -y install sshpass \
    && curl -fL -o docker.tgz "https://download.docker.com/linux/static/test/x86_64/docker-20.10.19.tgz" \
    && tar --strip-components=1 -xvzf docker.tgz -C /usr/bin \
    && groupadd docker \
    && gpasswd -a jenkins docker

USER jenkins