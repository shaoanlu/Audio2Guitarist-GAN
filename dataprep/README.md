# Data Preparation
## Descriptions
This folder contains 
  1. Scripts for extracting audio features using [librosa](https://librosa.github.io/librosa/) and [CREPE pitch tracker](https://github.com/marl/crepe).
  2. Instructions (this README) for generating training data (ground truth data) using 3rd party open source projects.

Note: The dependencies required for data preparation are not specified in main page.

## Ground truth data generation

### 1. Hands binary masks
  - **Dependency:** [hand3d](https://github.com/lmb-freiburg/hand3d)
  - **Method:** Using hand3d to create binary masks as shown below. (1 mask per frame)
  - ![hbm](https://github.com/shaoanlu/Audio2Guitarist-GAN/raw/master/readme_ims/mask.jpg)
  - **Output format:**
    - `ims_mask/mask_[VIDEO_NAME]_frame[FRAME].jpg`.
    - ex: `./ims_mask/mask_TrnVideo123_frame456.jpg`.
### 2. Joints heatmaps
  - **Dependency:** OpenPose ([official](https://github.com/CMU-Perceptual-Computing-Lab/openpose) or [keras port](https://github.com/michalfaber/keras_Realtime_Multi-Person_Pose_Estimation))
  - **Method:** Using OpenPose to create joint heatmaps as shown below. (7 heatmaps per frame)
  - ![jbm](https://github.com/shaoanlu/Audio2Guitarist-GAN/raw/master/readme_ims/heatmap.jpg)
  - **Output format:**
    - `./ims_heatmap/heatmap[i]_[VIDEO_NAME]_frame[FRAME].jpg`. `[i]` = 0 ~ 6
    - ex: `./ims_heatmap/heatmap0_TrnVideo123_frame456.jpg`.
### 3. Fretboard mask
  - **Dependency:** None
  - **Method:** Hand label (segment) a binary mask of the fretboard for each training video from an averaged rgb image over all frames. Only segment out frets after the capo fret. (1 mask per video)
  - ![fbm](https://github.com/shaoanlu/Audio2Guitarist-GAN/raw/master/readme_ims/fretboard.jpg)
  - **Output format:**
    - `fretboard_masks/fretboard_masks_[VIDEO_NAME].jpg`.
    - ex: `fretboard_masks/fretboard_masks_TrnVideo123.jpg`.
### 4. RGB image
  - **Dependency**: None
  - **Method**: Save every frames as a rgb image. (1 image per frame)
  - **Output format:**
    - `ims_rgb/rgb_[VIDEO_NAME]_frame[FRAME].jpg`.
    - ex: `ims_rgb/rgb_TrnVideo123_frame456.jpg`.
  
## Feature extraction

### Audio features extraction
  - CQT, LogMel, LogMel (delta), Chroma, Chroma (delta), Pitch
    - Pitch features are extracted using [CREPE](https://github.com/marl/crepe), the remains are extracted using librosa.
    - Normalized to [0,1] (except delta features).
  - Code can be found in [librosa_feats_extraction.ipynb]().
  - Output files:
    - `./npy/[VIDEO_NAME]_cqt.npy`, `./npy/[VIDEO_NAME]_chroma.npy`, `./npy/[VIDEO_NAME]_logmelspec.npy`, and `./npy/[VIDEO_NAME]_pitch.npy`.
  
## Preprocessing
### Alignment
  - Align joint heatmaps, hand masks, and fretboard masks.
  - Code can be found in [align_heatmaps.ipynb]().
