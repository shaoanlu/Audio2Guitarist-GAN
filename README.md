# Audio2Guitarist-GAN
A two-stage generative adversarial network that generates images of guitarists playing guitar from audio.

## Descriptions
  [To be updated]

## Architecture
### Stage 1: Audio to binary mask  
  ![stage1_arch](https://github.com/shaoanlu/Audio2Guitarist-GAN/raw/master/readme_ims/stage1_arch.jpg)
### Stage 2: Binary mask to color image
  ![stage2_arch](https://github.com/shaoanlu/Audio2Guitarist-GAN/raw/master/readme_ims/stage2_arch.jpg)
  
## Result

### 1. Video output
  - **Case 1: Test on the same guitarist, 南澤大介.**
    - **Video 1: トゥ・ビー・ウィズ・ユー (acoustic guitar solo)**
      - Result video [here](https://drive.google.com/open?id=1GnDKuxnZTCC5_23AyzVGp0hmlylGojnI).
      - Source YouTube video [here](https://www.youtube.com/watch?v=23nEZocwINo).
    - **Video 2: 愛はかげろうのように (acoustic guitar solo)**
      - Result video [here](https://drive.google.com/open?id=1WWVdGX-XQsl48tGQaQR0b64BNxCNq6cv).
      - Source YouTube video [here](https://www.youtube.com/watch?v=fh879tYOsYc).
  - **Case 2: Test on different guitarist, 伍々慧. The playing style and recording are different from the training data.**
    - **Video 3: Autumn Leaves (early version) / Satoshi Gogo**
      - Result video [here](https://drive.google.com/open?id=1txtLXhXmdtCV2qE5cReXLJqNQkbdRBtv).
      - Source YouTube video [here](https://www.youtube.com/watch?v=F1nFu1lE9Hg).
    - **Video 4: I got rhythm / Satoshi Gogo**
      - Result video [here](https://drive.google.com/open?id=17JAQCfWU-gkzGDo4dQ0O9OBNr0-BqfIO).
      - Source YouTube video [here](https://www.youtube.com/watch?v=44g26JcKqHM).
      
###### Here are the official website of [南澤大介](http://www.bsvmusic.com) and [伍々慧](https://www.gogosatoshi.com).

### 2. Conditional output
The following gifs are result images generated from an audio that the model had never seen. 
  - Source video (audio): [tupliのテーマ (acoustic guitar solo) 作曲／編曲：南澤大介](https://www.youtube.com/watch?v=ApbNNhVVsG8)
  - Top to bottom: audio visualization, stage-1 output, stage-2 output, ground truth.

![blue](https://www.dropbox.com/s/3atfluro1piv5dl/tupli_blue_audiovis.gif?raw=1) ![olive](https://www.dropbox.com/s/85s4pxthxp2djlp/tupli_olive_audiovis.gif?raw=1) ![wine](https://www.dropbox.com/s/6hjcq4xy4ctkd11/tupli_wine_audiovis.gif?raw=1)

### 3. Pose-guided generation
The following gifs show outputs of 2nd-stage model given conditional poses. 
  - Source video (audio): [John Pizzarelli - "I Got Rhythm" (solo) at the Fretboard Journal](https://www.youtube.com/watch?v=vVNVJGLVFCk)
  - Top: Reference video; Middle: conditional hands input; Bottom: stage 2 output.

![JP_guided_pose1](https://www.dropbox.com/s/mldgg1yg194ntcj/jp_guided_pose_hires_01.gif?raw=1) ![JP_guided_pose2](https://www.dropbox.com/s/z1m6h7oxslysvgc/jp_guided_pose_hires_02.gif?raw=1)

## References
1. [Audio to Body Dynamics](https://arviolin.github.io/AudioBodyDynamics/)
2. [Pose guided person image generation](https://arxiv.org/abs/1705.09368)
3. [Deep Video Generation, Prediction and Completion of Human Action Sequences](https://arxiv.org/abs/1711.08682)
4. [Deformable GANs for Pose-based Human Image Generation](https://arxiv.org/abs/1801.00055)
5. [Skeleton-aided Articulated Motion Generation](https://arxiv.org/abs/1707.01058)
6. [Assessment of Student Music Performances Using Deep Neural Networks](http://www.mdpi.com/2076-3417/8/4/507)
7. [Dance Dance Convolution](https://arxiv.org/abs/1703.06891)
