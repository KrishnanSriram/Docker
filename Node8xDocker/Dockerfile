FROM debian:jessie
RUN apt-get update -y && apt-get upgrade -y && apt-get install -y \
    curl \
    git \
    python-software-properties \
    vim
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash - \
    && apt-get update -y && apt-get upgrade -y \
    && apt-get install -y nodejs \
    && node --version && npm --version
CMD echo "Debian Node is ready for use"