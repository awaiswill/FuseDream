# FuseDream

This repo contains code for paper ([paper link](https://arxiv.org/abs/2112.01573)):
**FuseDream: Training-Free Text-to-Image Generation with Improved CLIP+GAN Space Optimization**
by *Xingchao Liu, Chengyue Gong, Lemeng Wu, Shujian Zhang, Hao Su and Qiang Liu* from UCSD and UT Austin.
## Introduction
FuseDream uses pre-trained GANs (we support BigGAN-256 and BigGAN-512 for now) and CLIP to achieve high-fidelity text-to-image generation.
## Requirements
Please use `pip` or `conda` to install the following packages:
`PyTorch==1.7.1, torchvision==0.8.2, lpips==0.1.4` and also the requirements from [BigGAN](https://github.com/ajbrock/BigGAN-PyTorch).
## Getting Started
We transformed the pre-trained weights of BigGAN from TFHub to PyTorch. To save your time, you can download the transformed BigGAN checkpoints from:
https://drive.google.com/drive/folders/1nJ3HmgYgeA9NZr-oU-enqbYeO7zBaANs?usp=sharing
Put the checkpoints into `./BigGAN_utils/weights/`
Run the following command to generate images from text query:
`python fusedream_generator.py --text 'YOUR TEXT' --seed YOUR_SEED`
For example, to get an image of a blue dog:
`python fusedream_generator.py --text 'A photo of a blue dog.' --seed 1234`
The generated image will be stored in `./samples`
## Colab Notebook
For a quick test of *FuseDream*, we provide Colab notebooks for [*FuseDream*(Single Image)](https://colab.research.google.com/drive/17qkzkoQQtzDRFaSCJQzIaNj88xjO9Rm9?usp=sharing) and *FuseDream-Composition*(TODO).
