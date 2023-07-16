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
mkdir /media/leelabsg-storage0/GWAS_tutorial/YOUR_NAME
``` 

### 5. Copy the lassosum_script.R from the PRS_tutorial/lassosum folder
``` 
cp PRS/lassosum/lassosum_script.R YOUR_NAME
``` 

### 6. Read lassosum_script.R using nano and change YOUR_NAME using ^o(overwrite) and ^x(exit)
```
nano YOUR_NAME/lassosum_script.R
```

### 5. Run lassosum
```
nohup Rscript /home/leelabguest/YOUR_NAME/lassosum_script.R > /home/leelabguest/YOUR_NAME/nohup.out & 
```

### *Way to check whether the code is running properly 
```
ps
```
```
cat /home/leelabguest/YOUR_NAME/nohup.out 
```
