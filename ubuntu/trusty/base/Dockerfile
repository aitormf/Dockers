# Own Ubuntu base
FROM ubuntu:trusty

LABEL manteiner Aitor Martínez Fernández+aitor-martinez.fernandez@gmail.com


# install basic packages
RUN apt update && apt install -q -y \
    wget \
    sudo \
    nano \
    bash-completion \
    && rm -rf /var/lib/apt/lists/*

# install graphics packages
RUN apt update && apt install -q -y \
    binutils \
    mesa-utils \
    module-init-tools \
    x-window-system\
    && rm -rf /var/lib/apt/lists/*

# install gedit
RUN apt update && apt install -q -y \
    gedit \
    && rm -rf /var/lib/apt/lists/*
