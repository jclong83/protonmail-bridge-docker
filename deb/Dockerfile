FROM ubuntu:noble
LABEL maintainer="James Long <james@jclong.net>"

EXPOSE 25/tcp
EXPOSE 143/tcp

WORKDIR /protonmail

# Copy bash scripts
COPY gpgparams install.sh entrypoint.sh VERSION /protonmail/

# Install dependencies and protonmail bridge
RUN bash install.sh

ENTRYPOINT ["bash", "/protonmail/entrypoint.sh"]
