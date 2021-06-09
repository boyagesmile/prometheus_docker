# prometheus_docker
[Docker](https://registry.hub.docker.com/repository/docker/boyagesmile/prometheus) for [amov-lab/Prometheus](https://github.com/amov-lab/Prometheus) 

## Prerequisites
- Docker

## Start
Start Docker with 
```
docker run -it --privileged \
--rm \
--net=host \
--env=LOCAL_USER_ID="$(id -u)" \
--gpus all \
--device /dev/mem:/dev/mem --cap-add SYS_RAWIO \
-v /tmp/.X11-unix:/tmp/.X11-unix \
-v /var/run/dbus/system_bus_socket:/var/run/dbus/system_bus_socket \
-v /home/wby/.Xauthority:/root/.Xauthority \
-e DISPLAY=unix$DISPLAY \
-e GDK_SCALE \
-e GDK_DPI_SCALE \
boyagesmile/prometheus:v1 /bin/bash
```
## About Docker
* ubuntu 18.04
* cuda 10.2
* cudnn 8
* opencv 3.3.1
* torch 1.4.0
* torchvision 0.5.0

## Run Example
```
cd ~/Prometheus
conda activate py27
roslaunch prometheus_gazebo sitl.launch
```
