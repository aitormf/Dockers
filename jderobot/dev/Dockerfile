# Jderobot for developers
FROM aitormf/ubuntu:base

LABEL manteiner Aitor Martínez Fernández+aitor.martinez.fernandez@gmail.com


## ROS ##
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116

RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros-latest.list

## ZeroC ##
RUN echo deb http://zeroc.com/download/apt/ubuntu16.04 stable main > /etc/apt/sources.list.d/zeroc.list

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv 5E6DA83306132997

## Gazebo ##

RUN echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable xenial main" > /etc/apt/sources.list.d/gazebo-stable.list

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 67170598AF249743


## JdeRobot ##
RUN sh -c 'echo "deb http://jderobot.org/apt xenial main" > /etc/apt/sources.list.d/jderobot.list'

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv B0E7F58E82C8091DF945A0453DA08892EE69A25C



# install deps dev
RUN apt update && apt install -q -y \
    jderobot-deps-dev \
    && rm -rf /var/lib/apt/lists/*

RUN echo "source /opt/ros/kinetic/setup.bash" >> /root/.bashrc 


CMD ["bash"]
