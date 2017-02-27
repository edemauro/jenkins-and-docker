FROM jenkins:2.32.2

ENV JAVA_OPTS="-Xmx8192m"

USER root
RUN mkdir /var/log/jenkins
RUN chown -R jenkins:jenkins /var/log/jenkins
USER jenkins