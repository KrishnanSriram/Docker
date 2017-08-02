FROM krishnansriram/debian_node8:1.0
RUN apt-get -y upgrade && apt-get -y update \
    && curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - \
    && echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list \
    && apt-get update && apt-get install yarn && yarn --version
RUN yarn global add @angular/cli && ng --version
CMD "Angular CLI is now available."
