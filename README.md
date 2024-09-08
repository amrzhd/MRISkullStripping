# MRI Skull Stripping Using UNet3D

## Project Overview

This project involves the development of a deep learning model for MRI skull stripping using the Calgary Campinas 359 dataset. The primary goal is to accurately segment brain tissue from MRI scans, which is a crucial preprocessing step for many neuroimaging studies.

## Dataset
T1-weighted volumetric brain MR images used in this project is sourced from the [Calgary Campinas 359 Dataset](https://portal.conp.ca/dataset?id=projects/calgary-campinas)
- 359 Participants
- Acquisition matrix size 256 x 218 x [170,180]
- 1.5 T and 3 T Magnetic Field Strength
- Voxel size for images is 1 mm³
  
## Model
The model used in this project is a 3D version of the UNet architecture, designed to handle volumetric data such as MRI scans. UNet3D is known for its encoder-decoder structure, which is particularly effective for segmentation tasks in 3D medical imaging.

![UNet3D Structure](https://drive.google.com/uc?export=view&id=1V6rL5vy5NQUCQxXu-xWdcCd-9f2kVmQu)

### Training Setup
- Optimizer: Adam
- Batch size: 64
- Epochs: 500
- Learning Rate: 0.001
- Loss Function: Cross Entropy

## Requirements
To run the code in this repository, make sure you have the following dependencies installed:
- Python >=3.8
- PyTorch == 2.3 (verified working with 2.0 - 2.3, both for CPU and GPU)
- torch-summary == 1.4.5
- nibabel == 5.2.1
- monai == 1.3.2
- scikit-learn >= 0.20.1
- matplotlib >= 2.2.3
  
## References
If you use this code or the UNet model architecture in your work, please cite the original paper of the orignal model:

[O. Ronneberger, P. Fischer, and T. Brox, "U-Net: Convolutional Networks for Biomedical Image Segmentation," arXiv preprint arXiv:1505.04597, 2015.](https://arxiv.org/abs/1505.04597)

If you used the dataset in your work, please cite the original paper of it:

[R. Souza, O. Lucena, J. Garrafa, D. Gobbi, M. Saluzzi, S. Appenzeller, L. Rittner, R. Frayne, and R. Lotufo, "An open, multi-vendor, multi-field-strength brain MR dataset and analysis of publicly available skull stripping methods agreement," NeuroImage, vol. 170, pp. 482-494, 2018, doi: 10.1016/j.neuroimage.2017.08.021.](https://www.sciencedirect.com/science/article/abs/pii/S1053811917306687?via%3Dihub)
