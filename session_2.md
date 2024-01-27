# Tutorial Session #2: PRS-CS

In this session, we are going to construct polygenic risk score using PRS-CS. \
References : [PRS-CS github](https://github.com/getian107/PRScs), [PRS-CS paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6467998/). \
The data we are going to use are already preprocessed or downloaded.

### 0. Log in to leelabguest
``` 
ssh leelabguest@147.47.200.131 -p 22555
```

### 1. Connect CPU
``` 
ssh leelabsg[01-07]
``` 

### 5. Calculate PRS using plink 
``` 
./plink \
--bfile /media/leelabsg-storage0/PRS_tutorial/data/plink/sample \
--score YOUR_DIRECTORY/prscs_chr1-22.txt 2 4 6 \
--out YOUR_DIRECTORY/score
``` 

### 3. Run PRS-CS 
``` 
python /media/leelabsg-storage0/PRS_tutorial/PRScs/PRScs.py \
--ref_dir=/media/leelabsg-storage0/PRS_tutorial/data/reference/ldblk_1kg_eas \
--bim_prefix=/media/leelabsg-storage0/PRS_tutorial/data/plink/sample \
--sst_file=/media/leelabsg-storage0/PRS_tutorial/data/summary_stat/sumstats_prscs.txt \
--n_gwas=177415 \
--out_dir=YOUR_DIRECTORY/PRScs
``` 

### 4. Merge chr1 - chr22 beta files into one file 
``` 
for i in {1..22}; do cat "YOUR_DIRECTORY/PRScs_pst_eff_a1_b0.5_phiauto_chr$i.txt" >> YOUR_DIRECTORY/prscs_chr1-22.txt; done
``` 

### 5. Calculate PRS using plink 
``` 
/home/n1/leelabguest/plink \
--bfile /media/leelabsg-storage0/PRS_tutorial/data/plink/sample \
--score YOUR_DIRECTORY/prscs_chr1-22.txt 2 4 6 \
--out YOUR_DIRECTORY/score
```

### 6. Check PRS score
``` 
head YOUR_DIRECTORY/score
``` 

