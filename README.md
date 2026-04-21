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
git clone https://github.com/holmeben/ros2-mac-native.git
```

Setup the Pixi environment.
```
pixi install -e clang-17
```

Enter the Pixi shell.
```
pixi shell -e clang-17
source install/setup.zsh # You must run this manually due to a Pixi bug
```

Create the ROS2 package source directory.
```
mkdir src
```

Then clone the required packages into `src` and run the appropriate `colcon build` command from the workspace root directory.
