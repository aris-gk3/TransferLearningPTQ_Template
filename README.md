# Project README

## Getting Started

Everything is based on the package from [this repo](https://github.com/aris-gk3/ml_project_util). It is installed below.

``` python
# In cloud engines/environments
!pip install git+https://github.com/aris-gk3/ml_project_util.git
# In local environments
pip install git+https://github.com/aris-gk3/ml_project_util.git
```

Setup step (change .env paths or set relative dataset path in cloud environment), as shown [here](https://github.com/aris-gk3/ml_project_util). 
1. Find head structure & data augmentation strategy
2. Train (unfreeze head and/or last block)
3. Find ranges of weights, bias & activation (Visualize optionally)
4. PTQ (3 methods) & Evaluate

> Example code for many utilities is given in [Modular Notebooks/](./data/).

> Full examples for 5 datasets are in [End-to-End Notebooks/](./End-to-End/) .


## Workflow

1. Dataset & Test Split  
Add images in classes
2. Apply Transfer Learning to VGG-16  
a. Set new head freeze other layers and train  
b. If needed, unfreeze some more layers & train  
3. Apply PTQ and evaluate  
Code iteratively finds appropriate ranges for quantization.
Calculations are made for HW efficient quantization. In this, multiply and add operations for scaling between layers is substituted with bit shifting by adjusting the ranges of each layer.
