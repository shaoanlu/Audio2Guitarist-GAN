# Audio2Guitarist-GAN
A two-stage generative adversarial network that generates images of guitarists playing guitar from audio.

## Descriptions
  [To be updated]

## Architecture
### Stage 1: Audio to binary mask  
  ![stage1_arch](https://github.com/shaoanlu/Audio2Guitarist-GAN/raw/master/readme_ims/stage1_arch.jpg)
### Stage 2: Binary mask to color image
  [To be updated]
  
## Result

### 1. Video output
[TBU]

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
