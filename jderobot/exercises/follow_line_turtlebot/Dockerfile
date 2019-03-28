FROM ubuntu:xenial

SHELL ["/bin/bash", "-c"]

### REPOSITORIES ###
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros-latest.list

RUN sh -c 'echo deb http://zeroc.com/download/apt/ubuntu16.04 stable main > /etc/apt/sources.list.d/zeroc.list'
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv 5E6DA83306132997

RUN sh -c 'echo "deb http://jderobot.org/apt xenial main" > /etc/apt/sources.list.d/jderobot.list'
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv 24E521A4

RUN echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable xenial main" > /etc/apt/sources.list.d/gazebo-stable.list
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 67170598AF249743


### DEPS ### 

# PYTHON ##
RUN apt update && apt install -y python-all python-pip && rm -rf /var/lib/apt/lists/*

RUN pip2 install --upgrade pip

RUN pip install  pyyaml

RUN apt update && apt-get install -y \ 
    python-matplotlib python-pyqt5 python-pip python-numpy python-pyqt5.qtsvg python-pyqt5.qsci nano\
    && rm -rf /var/lib/apt/lists/*

    
# JDEROBOT #
RUN apt update && apt-get install -y jderobot-config-python && rm -rf /var/lib/apt/lists/*

# ROS & OPENCV #
RUN apt update && apt install -q -y \
    ros-kinetic-roscpp ros-kinetic-std-msgs ros-kinetic-cv-bridge ros-kinetic-image-transport \
    ros-kinetic-roscpp-core ros-kinetic-rospy ros-kinetic-nav-msgs ros-kinetic-geometry-msgs \
    ros-kinetic-rosbash ros-kinetic-message-filters ros-kinetic-opencv3 \
    && rm -rf /var/lib/apt/lists/*

RUN apt update && apt install -q -y \
    ros-kinetic-kobuki ros-kinetic-kobuki-core ros-kinetic-robot-state-publisher \ 
    ros-kinetic-rplidar-ros ros-kinetic-urg-node \
    ros-kinetic-openni2-camera ros-kinetic-openni2-launch\
    && rm -rf /var/lib/apt/lists/*


### FILES ###

COPY turtlebot-hokuyo.launch /root/
COPY turtlebot-rplidar.launch /root/
COPY turtlebot-xtion.launch /root/


### CONFIG ###
WORKDIR /root/


RUN apt update && apt install -q -y ros-kinetic-realsense-camera ros-kinetic-librealsense && rm -rf /var/lib/apt/lists/*

RUN echo "source /opt/ros/kinetic/setup.bash" >> .bashrc
#RUN echo "source /opt/jderobot/setup.bash" >> .bashrc

