# Tutorial Session #1: Lassosum

In this session, we are going to construct polygenic risk score using Lassosum. \
References : [Lassosum github](https://github.com/tshmak/lassosum), [Lassosum paper](https://onlinelibrary.wiley.com/doi/abs/10.1002/gepi.22050). \
The data we are going to use are already preprocessed or downloaded.

### 0. Log in to leelabguest
``` 
ssh leelabguest@147.47.200.131 -p 22555
```

### 1. Activate conda environment
``` 
conda activate r_env
``` 

### 2. Make directory for practice session in your directory
``` 
mkdir YOUR_DIRECTORY
``` 

### 3. Copy the lassosum_script.R from the PRS_tutorial/lassosum folder
``` 
cp PRS_tutorial/lassosum/lassosum_script.R YOUR_DIRECTORY
``` 

### 4. Read lassosum_script.R using nano and change YOUR_DIRECTORY using ^o(overwrite) and ^x(exit)
```
nano YOUR_DIRECTORY/lassosum_script.R
```

### 5. Run lassosum
```
nohup Rscript YOUR_DIRECTORY/lassosum_script.R > YOUR_DIRECTORY/nohup.out & 
```

### *Way to check whether the code is running properly 
```
ps
```
```
cat YOUR_DIRECTORY/nohup.out
```

### 6. Move to your directory 
```
cd YOUR_DIRECTORY
```

### 7. Check the result from R
```
R
```
```
v <- readRDS("v.RDS")
result <- v[["results.table"]]
```
