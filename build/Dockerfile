
FROM ubuntu:xenial
MAINTAINER Max Belyanin <maxbelyanin@gmail.com>

RUN adduser tftpd \
	&& mkdir /tftp \
	&& chown tftpd:tftpd /tftp \
	&& apt-get update \
 	&& apt-get install -y tftpd-hpa \
	&& rm -rf /var/lib/apt/lists/*

ENTRYPOINT ["/usr/sbin/in.tftpd", "--foreground", "--address 0.0.0.0:69", "--secure /tftp"]
