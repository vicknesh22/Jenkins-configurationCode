FROM jenkins/jenkins:lts

LABEL maintainer="vicknesh22@gmail.com"
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt

ENV JENKINS_HOME /var/jenkins_home

ARG JAVA_OPTS
ENV JAVA_OPTS "-Djenkins.install.runSetupWizard=false ${JAVA_OPTS}"
RUN /bin/bash -c xargs /usr/local/bin/install-plugin.sh < /usr/share/jenkins/ref/plugins.txt
