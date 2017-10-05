# docker-tftp

## build

```console
docker build -t maxbelyanin/tftp .
```

## docker-compose example:

```yaml

version: '2'
services:

  tftp:
    image: maxbelyanin/tftp:ubuntu
    container_name: tftp
    ports:
      - "0.0.0.0:69:69"
    restart: always
    volumes:
      - ./tftp:/var/tftpboot
```

## Directory Tree

```console
./
|-- docker-compose.yml
|-- tftp
```
