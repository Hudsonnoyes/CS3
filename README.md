# project-3

Goal: This file serves as an orientation to everyone who comes to your repository, it should enable them to get their bearings.
Use markdown headers to divide content.

## Section 1: Software & Platform
This project was developed using the following software and tools:

Software Used:

[Python]
[UVA Rivanna HPC]

Add-On Packages:

[NUMPY] - [array operations]
[NIBABEL] - [accessing NIfTI]
[SCIKIT-LEARN] [data splitting / metrics]
[TQDM] - [progress bars]
[PANDAS] - [CSV logging]
[PYTORCH] - [core deep learning library]
[TORCHVISION] - [tensor utilities]
[CUDATOOLKIT] - [CUDA runtime]
[MONAI] - [medical imaging toolkit]

Platform Compatibility:

✅ Windows
✅ macOS (used during project)
✅ Linux

Ensure you have the required software installed before proceeding.

## Section 2: Directory
Below is a map of the repository, illustrating the hierarchy of files and folders:

📂 project-3/ 

│-- 📂 DATA/ 

│  │-- ```data_import_process.md``` # instructions to import KiTS23 dataset using their official repo

│  │-- ```deep_results.csv``` # raw results of DeepLabV3+ testing

│  │-- ```deeplabv3p_mobilenet2d.pth``` # saved weights after 30 epochs of training

│  │-- ```requirements.txt``` # required packages

│-- 📂 OUTPUT/

│  │-- ```metrics_plot.jpg``` # box plot comparing performances of nnUNet and DeepLabV3+ and displaying t-Test significance

│-- 📂 SCRIPTS/

│  │-- 📂 DeepLabV3+/

│  │  │-- 📂 Preprocessing/

│  │  │  │-- ```data_reorg.py``` # (1) separates images from masks/labels and only takes first 110 cases

│  │  │  │-- ```data_split.py``` # (2) splits data 64/16/20 (train/validate/test)

│  │  │  │-- ```data_slice.py``` # (3) reshapes *.nii.gz images and slices them into (512, 512) *.npy slices

│  │  │-- 📂 Info/

│  │  │  │-- ```Deep_paper.pdf```

│  │  │  │-- ```Deep_architecture.jpg```

│  │  │-- ```deeplab.py``` # training code, 30 epochs

│  │  │-- ```deep_test.py``` # testing code, outputs ```deep_results.csv```

│  │-- 📂 nnUNet/

│  │  │-- 📂 Preprocessing/

│  │  │-- 📂 Info/

│  │  │  │-- ```UNet_paper.pdf```

│  │  │  │-- ```UNet_architecture.jpg```

│  │  │-- ```unet.py```

|-- LICENSE.md

|-- README.md

## Section 3: Reproduction Steps
In this section, you should give explicit step-by-step instructions to reproduce the Results of your study. These instructions should be written in straightforward plain English, but they must be concise, but detailed and precise enough, to make it possible for an interested user to reproduce your results without much difficulty. N.B. This section will be crucial for the CS1 assignment, where you'll be required to reproduce the results of other groups. Therefore, make sure to explain this section thoroughly. 

### Part 1: Acquiring Data

1. Follow ```data_import_process.md```
