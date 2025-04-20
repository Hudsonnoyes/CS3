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

## Section 2: Documentation Map
Below is a map of the repository, illustrating the hierarchy of files and folders:

📂 project-3/ 
│-- 📂 DATA/ # Stock price data in csv form from 1999-12-31 - 2025-03-21
│-- 📂 OUTPUT/ # results of analysis performed on data, showing regression model test against data after 2020-04-01 │ │-- README.md # This orientation file
│-- 📂 SCRIPTS/ # Code for data processing, training, testing, and analysis │ 
    │-- preliminar_plots.py # Pull data using Alpha Vantage API and store in CSV files for each ticker │ 
    │-- data_preprocessing.py # Data cleaning and normalizing │ │-- model_training.py # training, testing, and analyzing data │-- 📂 RESULTS/ # Output files (graphs) 
|-- LICENSE.md
|-- README.md



## Section 3: Reproduction Steps
In this section, you should give explicit step-by-step instructions to reproduce the Results of your study. These instructions should be written in straightforward plain English, but they must be concise, but detailed and precise enough, to make it possible for an interested user to reproduce your results without much difficulty. N.B. This section will be crucial for the CS1 assignment, where you'll be required to reproduce the results of other groups. Therefore, make sure to explain this section thoroughly. 
