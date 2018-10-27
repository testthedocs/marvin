FROM python:3-alpine

LABEL maintainer "Sven <sven@testthedocs.org>" \
    org.label-schema.vendor = "TestTheDocs"

# Copy scripts, etc
COPY dockerfiles/Makefile /srv/Makefile
COPY dockerfiles/entrypoint.sh /usr/local/bin/entrypoint.sh
COPY cookiecutters /srv/cookiecutters

# Volume
VOLUME ["/srv/data"]

# Run commands
RUN builddeps=' \
    git \
    ' \
    && adduser -s /bin/false -D ttd \
    && apk --no-cache add \
    $builddeps \
    make \
    su-exec \
    tini \
    bash \
    ncurses \
    && pip3 install --no-cache-dir --upgrade pip \
    && pip3 install --no-cache-dir --upgrade setuptools \
    && pip3 install --no-cache-dir cookiecutter \
    && git clone https://github.com/testthedocs/cookiecutter-plone-training /srv/cookiecutters/cookiecutter-plone-training \
    && apk del --purge $builddeps

WORKDIR /srv

ENTRYPOINT ["/sbin/tini", "--", "/usr/local/bin/entrypoint.sh"]
