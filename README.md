# ROS2 Mac Native

## Setup
First install [Pixi](https://pixi.prefix.dev/latest/installation).

Create a directory for your ROS2 workspace.
```
mkdir ros2_ws
```

Clone the repository.
```
cd ros2_ws
git clone https://github.com/holmeben/ros2-mac-native.git .
```

Setup the Pixi environment.
```
pixi install
```

Enter the Pixi shell.
```
pixi shell
```

Create the ROS2 package source directory.
```
mkdir src
```

Then clone the required packages into `src` and run the appropriate `colcon build` command from the workspace root directory.
Then run `source setup.sh`. This must be done after any new build.

## Run
Run ROS2 commands as standard. On first launch, the Gazebo simulator may be slow to start. There may also be firewall permission popups, which should all be approved.

## Known Issues (and workarounds)
When running RViz, use `environment:=real` instead of `environment:=sim`. The sim preset loads the camera by default which causes a crash.
The camera can be viewed via RQT instead of RViz.

If the robot is not moving in the simulator, firewall settings may need to be adjusted.

If the robot is moving erratically in the simulator (rare), restart the terminal.
