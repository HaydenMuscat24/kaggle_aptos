# Aptos Challenge

9417 Kaggle project.

## Folder Structure:
- 'aptos2019' current train/test data (20gb zipped)
- 'aptos2015' old comp train/test data (80gb zipped)

### AWS instance
p2.xlarge with > 100gb, the cheapest being in N. Virginia or Ohio.
`pip install --upgrade pip`  
`pip install kaggle`  
`sudo apt install p7zip-full`  
`source activate tensorflow_p36`  
`git clone https://github.com/HaydenMuscat24/kaggle_aptos.git`  

### Azure instance instance
NC6 promo instance, with the data science vm (dsvm). 
`sudo -i`  
`pip install --upgrade pip`  
`sudo yum install p7zip-full`  
`pip install kaggle opencv-python`  
`git clone https://github.com/HaydenMuscat24/kaggle_aptos.git`  
The OS disk only has 30GB of space. us `fd -h` and look for the mount of the 100GB disk to place the data in and `ln -s` the disk to be under the git in the original OS. There is also a 350GB disk but that is removed when the instance is stopped.

## Kaggle api
Instructions at https://github.com/Kaggle/kaggle-api.  
`mkdir ~/.kaggle`  
`vim ~/.kaggle/kaggle.json`  
Place in the contents from your Kaggle api json  
`chmod 600 ~/.kaggle/kaggle.json`  

### aptos2019 data
Accept the rules https://www.kaggle.com/c/diabetic-retinopathy-detection/data/.   
`mkdir aptos2019 && cd aptos2019`  
`kaggle competitions download -c aptos2019-blindness-detection`  
`unzip test_images.zip -d test_images && unzip train_images.zip -d train_images && rm *.zip`

### aptos2015 data
Accept the rules https://www.kaggle.com/c/diabetic-retinopathy-detection/data.  
`mkdir aptos2015 && cd aptos2015`  
`kaggle competitions download -c diabetic-retinopathy-detection`  

`mkdir test_images train_images && mv test.zip* test_images && mv train.zip* train_images`  
`cd train_images && 7za x train.zip.001 && rm *.zip.* && mv train/* . && rmdir train && cd ..`  
`cd test_images  && 7za x test.zip.001  && rm *.zip.* && mv test/*  . && rmdir test  && cd ..`  

`unzip sampleSubmission.csv.zip && unzip trainLabels.csv.zip && unzip sample.zip && rm *.zip`  

