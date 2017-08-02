FROM debian:jessie
RUN apt-get update -y && apt-get upgrade -y && apt-get install -y \
    curl \
    git \
    python-software-properties \
    vim
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash -
RUN apt-get update -y && apt-get upgrade -y && apt-get install -y nodejs && node --version && npm --version
RUN npm install -g nodemon && mkdir -p /var/app/src && cd /var/app/src && git clone https://github.com/KrishnanSriram/GrangeAgentScannerService.git
EXPOSE 3000
RUN cd /var/app/src/GrangeAgentScannerService && npm install
CMD cd /var/app/src/GrangeAgentScannerService; npm start