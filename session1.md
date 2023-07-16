# Tutorial Session #1: Lassosum

In this session, we are going to construct polygenic risk score using Lassosum. \
References : [Lassosum github](https://github.com/tshmak/lassosum), [Lassosum paper](https://onlinelibrary.wiley.com/doi/abs/10.1002/gepi.22050). \
The data we are going to use are already preprocessed or downloaded.

### 0. Log in to leelabguest
``` 
ssh leelabguest@147.47.200.192
```

### 1. Connect CPU
``` 
ssh leelabsg[08-11]
``` 

### 2. Activate conda environment
``` 
conda activate r_env
``` 

### 4. Make directory for practice session in your directory
``` 
mkdir /media/leelabsg-storage0/PRS_tutorial/YOUR_DIRECTORY
``` 

### 5. Copy the lassosum_script.R from the PRS_tutorial/lassosum folder
``` 
cp /media/leelabsg-storage0/PRS_tutorial/lassosum/lassosum_script.R /media/leelabsg-storage0/PRS_tutorial/YOUR_DIRECTORY
``` 

### 6. Read lassosum_script.R using nano and change YOUR_DIRECTORY using ^o(overwrite) and ^x(exit)
```
nano /media/leelabsg-storage0/PRS_tutorial/YOUR_DIRECTORY/lassosum_script.R
```

### 7. Run lassosum
```
nohup Rscript /media/leelabsg-storage0/PRS_tutorial/YOUR_DIRECTORY/lassosum_script.R > /media/leelabsg-storage0/PRS_tutorial/YOUR_DIRECTORY/nohup.out & 
```

### *Way to check whether the code is running properly 
```
ps
```
```
cat /home/leelabguest/YOUR_DIRECTORY/nohup.out 
```
