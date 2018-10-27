FROM
LABEL maintainer "TestTheDocs <info@testthedocs.org>" \
    org.label-schema.vendor = "TestTheDocs"

# If we need ENVs set them here

# If possible first 'copy' for better cache and speed
COPY dockerfiles/entrypoint.sh /usr/local/bin/entrypoint.sh
COPY dockerfiles/check.sh /usr/local/bin/check.sh

# Second add 'run' commands

RUN
