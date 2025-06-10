# Project README

### Before Getting Started


* .env should be added with the following paths in the root directory:  
BASE_PATH, PATH_DATASET, PATH_TEST, PATH_RAWDATA, PATH_JOINEDDATA, PATH_SAVEDMODELS   

The folder structure presented below should be followed.


* This project goes hand to hand with [ml_project_util](https://github.com/aris-gk3/ml_project_util) . This package is installed as below.

``` python
# In cloud engines/environments
!pip install git+https://github.com/aris-gk3/ml_project_util.git
# In local environments
pip install git+https://github.com/aris-gk3/ml_project_util.git
```


### Workflow for getting started with new project

1. Dataset & Test Split  
Add images in classes
2. Apply Transfer Learning to VGG-16  
a. Set new head freeze other layers and train  
b. If needed, unfreeze some more layers & train  
3. Apply PTQ and evaluate  
Code iteratively finds appropriate ranges for quantization.
Calculations are made for HW efficient quantization. In this, multiply and add operations for scaling between layers is substituted with bit shifting by adjusting the ranges of each layer.


### Dataset & Test Split 

In both Tran_val & Test directories, images are contained in 1 subdirectory per class.

### Preproccessing

VGG-16 takes as input _224x224x3_, where 3 stands for BGR.

Choose appropriate Data Augmentation strategy.


**Add example code**