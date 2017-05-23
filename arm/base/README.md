JdeRobot ARM Ubuntu Image
========

This is a image of Ubuntu with basic packages, can be used to try JdeRobot package installation. This image depends on  [ARM Ubuntu image](https://hub.docker.com/r/armhf/ubuntu/)

It contains:
* wget, sudo, bash-completion packages
* binutils, mesa-utils, module-init-tools, x-window-system graphics packages
* Nano and gedit TextEditors installed ...

Before to exec this image you should run:

```apt-get update && apt-get install -y --no-install-recommends \
    qemu \
    qemu-user-static \
    binfmt-support
update-binfmts --enable qemu-arm
update-binfmts --display qemu-arm
```


# Usage
* Download: 
```sh
docker pull jderobot/ubuntu:arm-base
```
* run without GUI: 
```sh
docker run -ti jderobot/ubuntu:arm-base bash
```
* run with GUI: 
```sh
xhost +local:root
docker run -it --env="DISPLAY" --env="QT_X11_NO_MITSHM=1" --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" jderobot/ubuntu:arm-base bash
```

