# CRA1_basic
Duckietown CRA1 Basic Augmented Reality Exercise

Instructions to reproduce results

### 1. Clone this repository and go to its directory
```bash
git clone https://github.com/lineojcd/CRA1_basic.git
cd CRA1_basic
```
### 2. Build docker image in Duckiebot
```bash
dts devel build -f --arch arm32v7 -H [ROBOT_NAME].local 
```

### 3. Run docker image in Duckiebot with the following options
```bash
docker -H [ROBOT_NAME].local run -it -e MAP_FILE=[MAP_FILENAME] -v /data/config/calibrations/:/code/catkin_ws/src/CRA1_basic/calibrations/ --rm --net=host --privileged duckietown/CRA1_basic:latest-arm32v7
```
Choice of MAP_FILENAME: [hud, calibration_pattern, lane].

# Credit
Credit to afdaniele for the image projection pipeline (https://github.com/duckietown/dt-core/blob/6285293fb05351a23dc936a3dd70d42e61bca379/packages/ground_projection/include/ground_projection/GroundProjection.py)
