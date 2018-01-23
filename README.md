## Acknowledgments

This repo is a fork of https://github.com/brainsam/pgbouncer

I would like to thank @brainsam for its work that I'm reusing here.

## Synopsis

**pgbouncer** is a popular, small connection pooler for Postgresql. This is yet another docker image with pgbouncer, based on alpine.

## Code Example
You can configure it by Environment variables:
```bash
$ docker run -d \
 --name=pgbouncer \
 -e DB_HOST=postgresql.example.com \
 -e DB_USER=admin \
 -e DB_PASSWORD=mypassword \
 guizmaii/pgbouncer:v1.8.1
```
Or You can mount config file into docker container:
```bash
$ docker run -d \
 --name pgbouncer \
 -v pgbouncer-config-file:/etc/pgbouncer/pgbouncer.ini \
 guizmaii/pgbouncer:v1.8.1
```

## Installation

```bash
$ docker pull guizmaii/pgbouncer:v1.8.1
```
## Configuration

All configuration parameters of pgbouncer are available both by *--env* (use the same keys in upper case) and by mounting pgbouncer.ini into container.

#### Troubleshooting

```
docker logs <your-pgbouncer-container-name>
```
