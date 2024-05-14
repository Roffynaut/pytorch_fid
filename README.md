#Modification of (https://github.com/mseitzer/pytorch-fid/) enabling the user to access subfolders when using FID. 

# Data and program
Clone the program to root directory.
```
git clone https://github.com/Roffynaut/pytorch_fid.git
```
# Install 
Install from pip:
```
pip install pytorch_fid
```
# Run
To run the program simply follow the example. Point to the folder with generated images and the original Ham10000 dataset. 
```
python -m pytorch_fid --device cuda:0 path/to/dataset1 path/to/dataset2 --resolution 256
```
`--resolution` will scale the images to the same value. Default is 256. Set resolution to be equal to the generated images. 
To run the program on GPU use `--device cuda:N` where 'N' is the number of GPUs available. 

# To use npz files.
NPZ files have been created for the HAM10000 dataset which speeds up calculation. The 256x256 and 384x384 versions can be found in the /npz folder. 
Make sure to use the corresponding resolution. 
To use these simply add the dataset to one of the paths. For example:
python -m pytorch_fid --device cuda:0 path/to/dataset1 npz/isic_256.npz
