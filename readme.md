# YoloColorParse_Data
This repo is dedicated to storing the results from the [YoloColorParse](https://github.com/MURDriverless/YoloColorParse) MATLAB script. This is also used as a learning tool/repo for git branching and pushing.

## Instructions
As this is used as an instructional repo and a storage repo, only pull requests from branches are accepted.

1. Branch the repo from the current master
2. Dump output textfiles to the `./frames` subfolder
3. Send a pull request on github for another member to review

`./frames` is populated with frames as an example.

## Data

Original images and bounding box data were sourced from MIT Driverless [cv-core
/
MIT-Driverless-CV-TrainingInfra](https://github.com/cv-core/MIT-Driverless-CV-TrainingInfra/tree/master/CVC-YOLOv3). The original training labels does not seperate traffic cones into individual colour classes.

This repository improves upon the original dataset by adding in the following class labels.

* `0` Blue
* `1` Oragne
* `2` Yellow
* `3` False Positive (including cones of other colours, or cases where there are no traffic cones within bounding box)

The image labels added follow the default [darknet](https://github.com/AlexeyAB/darknet) YOLO format. See the [YoloColorParse](https://github.com/MURDriverless/YoloColorParse) repository for more information on how the labels were added.

```
<object-class> <x_center> <y_center> <width> <height>
```

Note that the original bounding boxes were used from the MIT dataset.


## Contributors

Special thanks to people who participated in adding traffic cone colour labels.

* Andrew Huang
* Harry Pittock
* Jack McRobbie
* Joseph Leong
* Michelle Keane
* Mihai Blaga
* Steven Lee