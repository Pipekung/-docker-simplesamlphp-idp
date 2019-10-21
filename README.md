# Supported tags

- [`1.0.6`, `1.0`, `latest`]()

# Quick Start

To pull from docker hub:

```console
$ docker pull pipekung/simplesamlphp-idp
```

### Running

To simply run the container:

```console
$ docker run -d -p 8000:80 -v /path/to/project:/var/www/html pipekung/simplesamlphp-idp
```

### ... via [`docker stack deploy`](https://docs.docker.com/engine/reference/commandline/stack_deploy/) or [`docker-compose`](https://github.com/docker/compose)

Create file `stack.yml` or `docker-compose.yml`

``` yml
version: "3.1"
services:
  app:
    image: pipekung/simplesamlphp-idp
    volumes:
      - /path/to/project:/var/www/html
    ports:
      - 8000:80
```

Run docker stack deploy:

```console
$ docker stack deploy -c stack.yml simplesamlphp_idp
```

or docker-compose:

```console
$ docker-compose up -d
```
