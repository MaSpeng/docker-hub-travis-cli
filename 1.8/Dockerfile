FROM ruby:2.5-alpine

ENV TRAVIS_CLI_VERSION 1.8.8

# Install build dependencies
RUN apk add --no-cache --virtual .build-deps \
    gcc \
    libc-dev \
    make

# Install persistant dependencies
RUN apk add --no-cache --virtual .persistent-deps \
    git

RUN gem install travis --version "${TRAVIS_CLI_VERSION}" \
    && apk del .build-deps

ENTRYPOINT [ "travis" ]

CMD [ "--help" ]
