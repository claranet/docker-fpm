# fpm docker image

Run [fpm](https://github.com/jordansissel/fpm) inside [Docker](https://www.docker.com/).

## Docker Hub

[https://hub.docker.com/r/claranet/fpm/](https://hub.docker.com/r/claranet/fpm/)

## Usage

Run the following in your source code that you wish to package resides.

```shell
docker run --rm -v "$PWD:/source" -v /etc/passwd:/etc/passwd:ro --user=$(id -u):$(id -g) claranet/fpm -t rpm -s dir -n rpm-name .
```

The following alias lets you run `fpm` as normal.

```shell
alias fpm='docker run --rm -v "$PWD:/source" -v /etc/passwd:/etc/passwd:ro --user=$(id -u):$(id -g) claranet/fpm'
```
