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
    image: maxbelyanin/tftp
    container_name: tftp
    ports:
      - "69:69"
    restart: always
    volumes:
      - ./tftp:/tftp
```

## Directory Tree

```console
./
|-- docker-compose.yml
|-- tftp
```
