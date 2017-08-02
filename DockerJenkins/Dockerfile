FROM krishnansriram/debian_node8:1.0
RUN apt-get -y upgrade && apt-get -y update \
    && apt-get install -y chkconfig daemon net-tools psmisc wget
RUN echo "deb http://http.debian.net/debian jessie-backports main" | tee -a /etc/apt/sources.list \
    && apt-get -y update \
    && apt-get install -y -t jessie-backports openjdk-8-jdk
RUN cd /tmp && wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | apt-key add - \
    && wget https://pkg.jenkins.io/debian/binary/jenkins_2.72_all.deb
RUN cd /tmp && dpkg -i jenkins_2.72_all.deb && apt-get -y update
EXPOSE 8080
RUN service jenkins start
CMD echo "Installed jenkins. Connect on port 8080 to see it running."