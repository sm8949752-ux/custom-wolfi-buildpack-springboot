FROM ubuntu:22.04


ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y --no-install-recommends \
    sudo curl python3 python3-pip wget git bash-completion tar gzip \
    && apt-get clean && rm -rf /var/lib/apt/lists/*


RUN curl -sSL "https://github.com/buildpacks/pack/releases/download/v0.36.4/pack-v0.36.4-linux.tgz" \
    | tar -C /usr/local/bin/ --no-same-owner -xzv pack

