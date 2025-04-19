# Importing Data from KiTS23

**Tip: we used VSCode to import the data**

1. enter the following in your terminal. All data will be downloaded under a ```dataset/``` folder
```
git clone https://github.com/neheller/kits23
cd kits23
pip3 install -e .
kits23_download_data
```
2. this dataset is the raw data, which will be split (90/10) and cleaned automatically by each model script
