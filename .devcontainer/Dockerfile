FROM mcr.microsoft.com/devcontainers/universal:2-linux

ARG gcc_version="11"

RUN apt-get update && apt-get upgrade -y

RUN apt-get install -y bison build-essential cmake doxygen flex gcc-${gcc_version} g++-${gcc_version} git graphviz libcap-dev libcurl4-openssl-dev libdrm-dev libevdev-dev libgbm-dev libminiupnpc-dev libnotify-dev libnuma-dev libopus-dev libpulse-dev libssl-dev libwayland-dev libx11-dev libxcb-shm0-dev libxcb-xfixes0-dev libxcb1-dev libxfixes-dev libxrandr-dev libxtst-dev ninja-build npm udev wget xvfb libva-dev libappindicator3-dev

RUN update-alternatives --install \
    /usr/bin/gcc gcc /usr/bin/gcc-${gcc_version} 100 \
    --slave /usr/bin/g++ g++ /usr/bin/g++-${gcc_version} \
    --slave /usr/bin/gcov gcov /usr/bin/gcov-${gcc_version} \
    --slave /usr/bin/gcc-ar gcc-ar /usr/bin/gcc-ar-${gcc_version} \
    --slave /usr/bin/gcc-ranlib gcc-ranlib /usr/bin/gcc-ranlib-${gcc_version}
