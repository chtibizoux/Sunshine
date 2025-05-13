FROM mcr.microsoft.com/devcontainers/cpp:1-ubuntu-24.04

ARG REINSTALL_CMAKE_VERSION_FROM_SOURCE="4.0.2"
ARG DEBIAN_FRONTEND=noninteractive

COPY ./reinstall-cmake.sh /tmp/

RUN chmod +x /tmp/reinstall-cmake.sh && /tmp/reinstall-cmake.sh ${REINSTALL_CMAKE_VERSION_FROM_SOURCE}; \
    && rm -f /tmp/reinstall-cmake.sh

RUN apt-get update && apt-get upgrade -y

RUN chmod +x scripts/linux_build.sh && ./scripts/linux_build.sh
