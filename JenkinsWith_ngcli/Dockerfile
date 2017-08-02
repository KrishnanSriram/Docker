FROM krishnansriram/debian_jenkins:1.0
RUN apt-get -y upgrade && apt-get -y update \
    && npm install -g yarn \
    && yarn global add @angular/cli \
    && ng --version