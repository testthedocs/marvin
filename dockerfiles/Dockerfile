FROM python:3-alpine

LABEL maintainer "Sven <sven@testthedocs.org>" \
    org.label-schema.vendor = "TestTheDocs"

# Copy scripts, etc
COPY dockerfiles/Makefile /srv/Makefile
COPY dockerfiles/entrypoint.sh /usr/local/bin/entrypoint.sh

# Run commands
RUN adduser -s /bin/false -D -H ttd \
    && apk --no-cache add \
    make \
    su-exec \
    tini \
    bash \
    ncurses \
    && pip3 install --no-cache-dir --upgrade pip \
    && pip3 install --no-cache-dir --upgrade setuptools \
    && pip3 install --no-cache-dir cookiecutter

WORKDIR /srv

ENTRYPOINT ["/sbin/tini", "--", "/usr/local/bin/entrypoint.sh"]
