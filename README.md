# Kidney segmentation case study

## Data
All data necessary for the case study is in the Data folder.

## Scripts
Shows the code and scripts used to load and run the models

## AI and ML
An article meant to familiarize the participant with how machine learning is used in medical imaging

## CS3_Rubric
The rubric used for scoring case study submissions.

## Hook Document
The document that provides context on the case study and describes the deliverable.

## Training a classifier
Extremely important document: describes the process of training a classification model using pytorch

Software Used:

[Python]

[Jupyter Notebook]

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



📂 project-3/ 

│-- 📂 DATA/ 

│  │-- ```data_import_process.md``` # instructions to import KiTS23 dataset using their official repo

│  │-- ```deep_results.csv``` # raw results of DeepLabV3+ testing

│  │-- ```deeplabv3p_mobilenet2d.pth``` # saved weights of DeepLabV3+ after 30 epochs of training

│  │-- ```requirements.txt``` # required packages

│  │-- ```unet_results.csv``` # raw results of UNet testing

│  │-- ```two_layer_unet_epoch_13.csv``` # saved weights of UNet after 13 epochs of training


│-- 📂 SCRIPTS/

│  │-- 📂 Preprocessing/

│  │  │-- ```data_reorg.py``` # (1) separates images from masks/labels and only takes first 110 cases

│  │  │-- ```data_split.py``` # (2) splits data 64/16/20 (train/validate/test)

│  │  │-- ```data_slice.py``` # (3) reshapes *.nii.gz images and slices them into (512, 512) *.npy slices

│  │-- 📂 DeepLabV3+/

│  │  │-- 📂 Info/

│  │  │  │-- ```Deep_paper.pdf```

│  │  │  │-- ```Deep_architecture.jpg```

│  │  │-- ```deeplab.py``` # training code, 30 epochs

│  │  │-- ```deep_test.py``` # testing code, outputs ```deep_results.csv```

│  │-- 📂 UNet/

│  │  │-- 📂 Info/

│  │  │  │-- ```nnUNet_paper.pdf```

│  │  │  │-- ```nnUNet_architecture.jpg```

│  │  │-- ```unet.py``` # training code, 30 epochs

│  │  │-- ```unet_test.py``` # testing code, outputs ```unet_results.csv```

│  │-- ```analysis.ipynb``` #

|-- LICENSE.md

|-- README.md

## 
