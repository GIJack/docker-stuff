FROM debian:latest

LABEL maintainer="GI_Jack - <GI_Jack@hackermail.com>"
LABEL description="Hello World As a Service (HWaaS)"

EXPOSE 1337/tcp

RUN apt update
RUN apt install -y bash coreutils netcat-openbsd

COPY hello_world.sh /opt/hello_world.sh
COPY entrypoint.sh /entrypoint.sh

RUN chmod +x /opt/hello_world.sh

#ENTRYPOINT ['/entrypoint.sh']
CMD "/opt/hello_world.sh"
