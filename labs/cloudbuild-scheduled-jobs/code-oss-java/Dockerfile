
FROM us-central1-docker.pkg.dev/cloud-workstations-images/predefined/code-oss:latest

# Custom SSH server config
COPY sshd_config /etc/ssh/

# Upgrade everything
RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get -y dist-upgrade

RUN wget https://open-vsx.org/api/vscjava/vscode-java-debug/0.40.1/file/vscjava.vscode-java-debug-0.40.1.vsix && \
unzip vscjava.vscode-java-debug-0.40.1.vsix "extension/*" &&\
mv extension /opt/code-oss/extensions/java-debug

RUN wget https://open-vsx.org/api/vscjava/vscode-java-dependency/0.19.1/file/vscjava.vscode-java-dependency-0.19.1.vsix && \
unzip vscjava.vscode-java-dependency-0.19.1.vsix "extension/*" &&\
mv extension /opt/code-oss/extensions/java-dependency

RUN wget https://open-vsx.org/api/redhat/java/1.6.0/file/redhat.java-1.6.0.vsix && \
unzip redhat.java-1.6.0.vsix "extension/*" &&\
mv extension /opt/code-oss/extensions/redhat-java

RUN wget https://open-vsx.org/api/vscjava/vscode-maven/0.35.2/file/vscjava.vscode-maven-0.35.2.vsix && \
unzip vscjava.vscode-maven-0.35.2.vsix "extension/*" &&\
mv extension /opt/code-oss/extensions/java-maven

RUN wget https://open-vsx.org/api/vscjava/vscode-java-test/0.35.0/file/vscjava.vscode-java-test-0.35.0.vsix && \
unzip vscjava.vscode-java-test-0.35.0.vsix "extension/*" &&\
mv extension /opt/code-oss/extensions/java-test
