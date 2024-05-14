#Modification of (https://github.com/mseitzer/pytorch-fid/) enabling the user to access subfolders when using FID. 

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


