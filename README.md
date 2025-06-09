# Project README

Workflow for getting started with new project.

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