FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu

# use this Dockerfile to install additional tools you might need, e.g.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends python3-pip \
    && curl "https://awscli.amazonaws.com/awscli-exe-linux-aarch64.zip" -o "awscliv2.zip" \
    && unzip awscliv2.zip \
    && sudo ./aws/install --bin-dir /usr/local/bin --install-dir /usr/local/aws-cli --update \
    && python3 -m pip install --upgrade localstack awscli-local
