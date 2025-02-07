# Using the Kimera-VIO ROS wrapper with Docker

## Building and running your container
To build the container, in this directory, run the following:
```
docker build -t kimera_vio_ros:latest .
```
To run the container, run the following command. This script allows X11 forwarding, which allows Rviz to be used with the container.
```
./docker_test.bash [optional image name; default is kimera_vio_ros]
```

## Running the EuRoC demonstration with Rviz
For running the EuRoC demonstration with Rviz, follow the instructions [here](https://github.com/MIT-SPARK/Kimera-VIO-ROS?tab=readme-ov-file#online).

The bag file path you will need to specify is `/catkin_ws/V1_01_easy.bag`.

### Possible errors:
* If your trajectory tracking looks incorrect immediately, update the `autoInitialize` field from 0 to 1 in `/catkin_ws/src/Kimera-VIO/params/Euroc/BackendParams.yaml`.
* An X server should be installed on your local machine to allow Rviz to be used with the container.
