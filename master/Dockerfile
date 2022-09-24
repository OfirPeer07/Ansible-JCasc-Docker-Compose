FROM jenkins/jenkins:2.332.2

# Install plugins
COPY plugins_extra.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt

# Copy Jenkins config as code
COPY ./jenkins.yaml /var/jenkins_home/jenkins.yaml

# Set java options.
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false
