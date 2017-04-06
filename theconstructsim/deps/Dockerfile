
# trusty para ejecutar jderobot en trusty
FROM aitormf/construct:trusty

LABEL manteiner Aitor Martínez Fernández+aitor.martinez.fernandez@gmail.com

# install dependencias basicas de compilacion de jderobot
RUN apt update && apt install -q -y \
    build-essential \
    libtool \
    cmake \
    g++ \
    gcc \
    git \
    make \
    && rm -rf /var/lib/apt/lists/*

# install dependencias de compilacion de jderobot
RUN apt update && apt install -q -y \
    ice35-slice \
    ice35-translators \
    libzeroc-ice35-dev \
    ice35-services \
    && rm -rf /var/lib/apt/lists/*


# install dependencias que faltan
RUN apt update && apt install -q -y \
    python-zeroc-ice \
    libicestorm35 \
    && rm -rf /var/lib/apt/lists/*


CMD ["bash"]