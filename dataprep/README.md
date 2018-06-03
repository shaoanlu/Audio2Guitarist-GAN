# Data Preparation
## Descriptions
This folder contains 
  1. Scripts for extracting audio features using [librosa](https://librosa.github.io/librosa/) and [CREPE pitch tracker](https://github.com/marl/crepe).
  2. Instructions (this README) for generating training data (ground truth data) using 3rd party open source projects.

Note: The dependencies required for data preparation are not specified in main page.

## Ground truth data generation

### 1. Hands binary masks
  - Dependency: [hand3d](https://github.com/lmb-freiburg/hand3d)
  - [TBU]
### 2. Joints heatmaps
  - Dependency: OpenPose ([official](https://github.com/CMU-Perceptual-Computing-Lab/openpose) or [keras port](https://github.com/michalfaber/keras_Realtime_Multi-Person_Pose_Estimation))
  - [TBU]
### 3. Finger knuckles masks (optional)
  - Dependency: OpenPose ([official](https://github.com/CMU-Perceptual-Computing-Lab/openpose) or [another keras port for hands](https://github.com/mmittek/openpose-keras))
  - [TBU]
