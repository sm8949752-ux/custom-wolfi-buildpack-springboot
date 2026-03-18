FROM mcr.microsoft.com/devcontainers/base:jammy

# Install Python and essential tools
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    curl \
    git \
    xz-utils \
    && rm -rf /var/lib/apt/lists/*

# Install pack CLI (Official Binary)
RUN curl -sSL "https://github.com/buildpacks/pack/releases/download/v0.36.4/pack-v0.36.4-linux.tgz" \
    | tar -C /usr/local/bin/ --no-same-owner -xzv pack

# Install Python UI libraries for local testing of your Buildpack scripts
RUN pip3 install rich tomli tomli-w