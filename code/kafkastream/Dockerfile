FROM debian:jessie

RUN echo "deb http://ftp.debian.org/debian testing main" >> /etc/apt/sources.list && \
    echo "deb http://ftp.de.debian.org/debian jessie-backports main" >> /etc/apt/sources.list && \
    apt-get update && \
    apt-get install -y openjdk-8-jre-headless openjdk-8-jdk

RUN apt-get install -y maven

RUN mkdir /myProject
WORKDIR /myProject

CMD ["mvn", "package"]
