# AnimeGAN

This repository contains my project I did in my Neural Networks & Applications course at IIT Kharagpur.\
The developed GAN architecture is used to transoform real-world images into their animated variants

## Results

These are some of the real images taken from IIT Kharagpur campus.

![Real Images](real_images/real_overall_result.png)

These are the transformed animated variants of the real images.

![Generated Images](test_output/gen_overall_result.png)

## Training:

The following command needs to be run in the terminal:

VGG-19 weight file is also required for the content loss. As this file is above 500 MB, we are providing the download link:

Download VGG-19 weights: https://download.pytorch.org/models/vgg19-dcbb9e9d.pth

python CartoonGAN.py --name your_project_name --src_data src_data_path --tgt_data tgt_data_path --vgg_model pre_trained_VGG19_model_path

## Testing:

The testing of the GAN network can be run from the trained model after 100 epochs.

python test.py --input_dir images --style Danbooru --gpu 0

## Hierarchy

The Input Data needs to be saved in this hierarchy.

├── data \
│   ├── src_data # src data (not included in this repo) \
│   |    ├── train \
│   |    └── test \
│   └── tgt_data # tgt data (not included in this repo)\
│       ├── train \
│       └── pair # edge-promoting results to be saved here \
│\
├── CartoonGAN.py # training code\
├── edge_promoting.py\
├── utils.py\
├── networks.py\
└── name_results # results to be saved here


## Requirements
PyTorch
OpenCV
