# Own ARM Ubuntu base
FROM armhf/ubuntu:xenial

LABEL manteiner Aitor Martínez Fernández+aitor-martinez.fernandez@gmail.com

COPY ./qemu-arm-static /usr/bin/ 

RUN apt-get update && apt-get install -q -y \
    bash \
    && rm -rf /var/lib/apt/lists/*

# install basic packages
RUN apt-get update && apt-get install -q -y \
    wget \
    sudo \
    nano \
    bash-completion \
    && rm -rf /var/lib/apt/lists/*

# install graphics packages
RUN apt-get update && apt-get install -q -y \
    binutils \
    mesa-utils \
    module-init-tools \
    x-window-system\
    gedit \
    && rm -rf /var/lib/apt/lists/*

# Enabling bash-completion
COPY ./completion /tmp/

RUN cat /tmp/completion >> /etc/bash.bashrc


