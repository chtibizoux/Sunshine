FROM mcr.microsoft.com/devcontainers/universal

WORKDIR /tmp/sunshine

COPY . .

RUN git submodule update --init --recursive && chmod +x scripts/linux_build.sh && ./scripts/linux_build.sh && rm -rf .