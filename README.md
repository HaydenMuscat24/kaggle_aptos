# Aptos Challenge

9417 Kaggle project.

##Folder Structure:
- 'aptos2019' current train/test data (20gv zipped)
- 'aptos2015' old comp train/tesr data (80gb zipped)
- folder for each person (should be no git issues, but can still access other peoples code. Strucutre yours how you feel like)
- 'resnet50' contains the base resnet NN weights
- submission.py will be what is provided to kaggle as a submission (along with relevant weights files)

## AWS instance
`source activate tensorflow_p36`  
`pip install tqdm`  
`pip install --upgrade pip`  
`source activate tensorflow_p36`  
`git clone https://github.com/HaydenMuscat24/kaggle_aptos.git`  

## Kaggle api
Instructions at https://github.com/Kaggle/kaggle-api. 
`pip install kaggle`  
`mkdir ~/.kaggle`  
`vim ~/.kaggle/kaggle.json`  
Place in the contents from your Kaggle api json 

### aptos2019 data
Accept the rules https://www.kaggle.com/c/diabetic-retinopathy-detection/data/.    
`kaggle competitions download -c aptos2019-blindness-detection`

### aptos2015 data
Accept the rules https://www.kaggle.com/c/diabetic-retinopathy-detection/data.  
`kaggle competitions download -c diabetic-retinopathy-detection`



##Todo:
- find a good way to automatically pip install required modules on a new system
