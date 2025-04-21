# project-3

Goal: This file serves as an orientation to everyone who comes to your repository, it should enable them to get their bearings.
Use markdown headers to divide content.

## Section 1: Software & Platform
This project was developed using the following software and tools:

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

│  │  │  │-- ```nnUNet_paper.pdf```

│  │  │  │-- ```nnUNet_architecture.jpg```

│  │  │-- ```unet.py``` # training code, 30 epochs

│  │  │-- ```unet_test.py``` # testing code, outputs ```unet_results.csv```

│  │-- ```analysis.ipynb``` #

|-- LICENSE.md

|-- README.md

## Section 3: Reproduction Steps
In this section, you should give explicit step-by-step instructions to reproduce the Results of your study. These instructions should be written in straightforward plain English, but they must be concise, but detailed and precise enough, to make it possible for an interested user to reproduce your results without much difficulty. N.B. This section will be crucial for the CS1 assignment, where you'll be required to reproduce the results of other groups. Therefore, make sure to explain this section thoroughly. 

### Part 1: Setting Up Environment/Workflow

1. We recommend running all steps in the Jupyter Notebook accessed through Rivanna
2. Set up your virtual environment with all dependencies from ```requirements.txt``` installed
3. Clone this repo

```
! git clone https://github.com/ali-rn/project-3/
```

### Part 2: Importing & Preprocessing Data

1. Follow ```data_import_process.md``` to obtain the dataset
2. Run ```data_reorg.py``` to rearrange image and labels data to match the input format of the mdoels and truncate dataset to 110 cases
3. Run ```data_split.py``` to split the dataset into 64/16/20 (train/validate/test)
4. Run ```data_slice.py``` to slice the 3D patient ```*.nii.gz``` volumes into 2D ```*.npy``` slices for faster, less expensive processing

### Part 3: Training the Models

1. Run ```deeplab.py``` and ```unet.py``` one at a time to train the two models
2. Run ```deep_test.py``` and ```unet.test.py``` to test the two models using the ```*.pth``` checkpoint weights saved from training. This will will generate two ```metrics.csv``` files

### Part 4: Analyzing Results

1. Run ```analysis.ipynb``` and input both ```*.csv``` files to generate the output boxplot
