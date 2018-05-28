# Audio2Guitarist-GAN
A two-stage generative adversarial network that generates images of guitarists playing guitar from audio.

## Descriptions
  [To be updated]

## Architecture
### Stage 1: Audio to binary mask  
  [To be updated]
### Stage 2: Binary mask to color image
  [To be updated]
  
## Result

### 1. Conditional output
The following gifs are result images generated from an audio that the model had never seen. (Top: ground truth; Middle: stage 1 output; Bottom: stage 2 output)
  - **Source video (audio): [tupliのテーマ (acoustic guitar solo) 作曲／編曲：南澤大介](https://www.youtube.com/watch?v=ApbNNhVVsG8)**

![blue](https://www.dropbox.com/s/b07rhz3mi51x77m/tupli_blue.gif?raw=1) ![plive](https://www.dropbox.com/s/zac7dho5o2v8o6a/tupli_green.gif?raw=1) ![wine](https://www.dropbox.com/s/r7n8ybyf4aawlgu/tupli_wine.gif?raw=1)

### 2. Pose-guided generation
The following gifs show outputs of 2nd-stage model given conditional poses. (Top: Reference video; Middle: conditional hands input; Bottom: stage 2 output.) 
  - **Source video (audio): [John Pizzarelli - "I Got Rhythm" (solo) at the Fretboard Journal](https://www.youtube.com/watch?v=vVNVJGLVFCk)**

![JP_guided_pose1](https://www.dropbox.com/s/mldgg1yg194ntcj/jp_guided_pose_hires_01.gif?raw=1) ![JP_guided_pose2](https://www.dropbox.com/s/z1m6h7oxslysvgc/jp_guided_pose_hires_02.gif?raw=1)
