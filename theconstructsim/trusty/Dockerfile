# trusty como the constructsim
FROM aitormf/trusty:base

LABEL manteiner Aitor Martínez Fernández+aitor.martinez.fernandez@gmail.com


## ROS ##
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116

RUN echo "deb http://packages.ros.org/ros/ubuntu trusty main" > /etc/apt/sources.list.d/ros-latest.list

RUN echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable trusty main" > /etc/apt/sources.list.d/gazebo-latest.list

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 67170598AF249743


# install deps dev
RUN apt update && apt install -q -y \
    libopencv-dev \
    python-opencv \
    ros-indigo-gazebo7-ros-pkgs \
    ros-indigo-gazebo7-ros-control \
    icebox \
    libpcl-1.7-all-dev \
    python-qt4-dev \
    pyqt5-dev \
    && rm -rf /var/lib/apt/lists/*


RUN echo "source /opt/ros/indigo/setup.bash" >> /root/.bashrc 


CMD ["bash"]
