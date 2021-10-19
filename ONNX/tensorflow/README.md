# Installation
```bash
# create the environment from environment.yml
conda env create -f environment.yml
# activate the conda environment
conda activate tensorflow
```

# Introduction

The convert.ipynb shows how to convert keras model and tensorflow saved_model to ONNX model.  
Pretrained Resnet50 model is used.  
Keras model can be converted both in command line style and python style,  
while saved_model uses command line style.  
The three generated onnx models predict the same result.

