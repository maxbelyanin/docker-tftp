
FROM ubuntu:xenial
MAINTAINER Max Belyanin <maxbelyanin@gmail.com>

RUN apt-get update \
 	&& apt-get install -y tftpd-hpa \
	&& rm -rf /var/lib/apt/lists/*

VOLUME /var/tftpboot
EXPOSE 69/udp
ENTRYPOINT ["in.tftpd"]
CMD ["-L", "--secure", "/var/tftpboot"]