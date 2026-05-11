FROM mcr.microsoft.com/devcontainers/universal:2

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    clang cmake ninja-build pkg-config libgtk-3-dev \
    liblzma-dev xz-utils curl unzip

# Install Flutter SDK
RUN git clone https://github.com/flutter/flutter.git -b stable /usr/local/flutter
ENV PATH="/usr/local/flutter/bin:${PATH}"

RUN flutter doctor
