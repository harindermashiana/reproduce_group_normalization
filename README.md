
# Assignment   - Final Project Group Normalization

This project aims to reproduce the results of the paper “Group Normalization” by Yuxin Wu and Kaiming He. The goal is to evaluate the effectiveness of Group Normalization (GN) in comparison to Batch Normalization (BN), Layer Normalization (LN) and Instance Normalization (IN) on the Tiny ImageNet-200 dataset and model architecture we created. 

# How to use this repo

You can read the report attached in this repository for greater insights into the project. The entire code to run and reproduce the results in the original paper can be found in this notebook training_results.ipynb


# Organization of this directory

TODO students: Run commands to create a directory tree, as described in previous assignments

```   
./
├── README.md
├── figures
│   ├── NNDL-hm3008-yl5444-zl3372_gcp_work_example_screenshot_1.png
│   ├── NNDL-hm3008-yl5444-zl3372_gcp_work_example_screenshot_2.png
│   └── NNDL-hm3008-yl5444-zl3372_gcp_work_example_screenshot_3.png
├── tiny-imagenet-200
|   ├── test/images
│   ├── train
│   ├── val
│   ├── wnids.txt
│   └── words.txt
├── utils
|    ├── GroupNormalization.py
|    └── InstanceNormalization.py
├── hist1.pkl
├── hist2.pkl
├── hist3.pkl
├── hist4.pkl
├── training_results.ipynb
├── requirements.txt
├──E4040.2023Fall.NNDL.report.hm3008.yl5444.zl3372.pdf

```
