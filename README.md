<img src='paper/shinjuku.jpg' align="left" width=1000>

<br><br><br>


- Tensorflow implementation for CVPR2020 paper “Learning to Cartoonize Using White-box Cartoon Representations”.
- Improved method for facial images are now available:
- https://github.com/SystemErrorWang/FacialCartoonization

<img src="images/method.jpg" width="1000px"/>
<img src="images/use_cases.jpg" width="1000px"/>

## Use cases

### Scenery
<img src="images/city1.jpg" width="1000px"/>
<img src="images/city2.jpg" width="1000px"/>

### Food
<img src="images/food.jpg" width="1000px"/>

### Indoor Scenes
<img src="images/home.jpg" width="1000px"/>

### People
<img src="images/person1.jpg" width="1000px"/>
<img src="images/person2.jpg" width="1000px"/>

### More Images Are Shown In The Supplementary Materials


## Online demo

- Some kind people made online demo for this project
- Demo link: https://cartoonize-lkqov62dia-de.a.run.app/cartoonize
- Code: https://github.com/experience-ml/cartoonize
- Sample Demo: https://www.youtube.com/watch?v=GqduSLcmhto&feature=emb_title

## Prerequisites

- Training code: Linux or Windows
- NVIDIA GPU + CUDA CuDNN for performance
- Inference code: Linux, Windows and MacOS


## How To Use

### Installation

- Assume you already have NVIDIA GPU and CUDA CuDNN installed 
- Install tensorflow-gpu, we tested 1.12.0 and 1.13.0rc0 
- Install scikit-image==0.14.5, other versions may cause problems


### Inference with Pre-trained Model

- Store test images in /test_code/test_images
- Run /test_code/cartoonize.py
- Results will be saved in /test_code/cartoonized_images


### Train

- Place your training data in corresponding folders in /dataset 
- Run pretrain.py, results will be saved in /pretrain folder
- Run train.py, results will be saved in /train_cartoon folder
- Codes are cleaned from production environment and untested
- There may be minor problems but should be easy to resolve
- Pretrained VGG_19 model can be found at following url:
https://drive.google.com/file/d/1j0jDENjdwxCDb36meP6-u5xDBzmKBOjJ/view?usp=sharing



### Datasets

- Due to copyright issues, we cannot provide cartoon images used for training
- However, these training datasets are easy to prepare
- Scenery images are collected from Shinkai Makoto, Miyazaki Hayao and Hosoda Mamoru films
- Clip films into frames and random crop and resize to 256x256
- Portrait images are from Kyoto animations and PA Works
- We use this repo(https://github.com/nagadomi/lbpcascade_animeface) to detect facial areas
- Manual data cleaning will greatly increace both datasets quality

## Acknowledgement
