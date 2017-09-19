FROM ruby:2.4.2

RUN apt-get update && apt-get install -y rpm && \
    apt-get clean && rm -rf /var/lib/apt/lists/*
RUN gem install fpm -v 1.9.3 --no-doc --no-ri

WORKDIR /source

ENTRYPOINT ["fpm"]

# see http://label-schema.org/rc1/
LABEL org.label-schema.name="fpm" \
      org.label-schema.version="1.9.3" \
      org.label-schema.description="fpm" \
      org.label-schema.vendor="Claranet UK" \
      org.label-schema.schema-version="1.0" \
      org.label-schema.vcs-url="https://github.com/claranet/docker-fpm" \
      org.label-schema.usage="https://github.com/claranet/docker-fpm/README.md \
      maintainer="pawel.fiuto@claranet.uk"
