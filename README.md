# Potato Leaf Disease Classification using Deep Learning

This project aims to classify potato leaf diseases using deep learning techniques. 
We will be using the 'plant-village dataset', which is available on Kaggle [Here](https://www.kaggle.com/datasets/arjuntejaswi/plant-village).

# Overview

This project aims to classify images of potato leaves into one of three categories:

1. Early Blight
2. Late Blight
3. Healthy
The project uses Convolutional Neural Networks (CNNs) to train a model to classify the images.

# Prerequisites

The following libraries are required to run the notebook:

1. opendatasets
2. split-folders
3. numpy
4. pandas
5. tensorflow
6. matplotlib
7. seaborn
8. scikit-learn
9. keras

You can install them using the following command:
`pip install opendatasets split-folders numpy pandas tensorflow matplotlib seaborn scikit-learn keras
`
# Installing
`
You can download the dataset using the following code:
dataset_url = 'https://www.kaggle.com/datasets/arjuntejaswi/plant-village'
import opendatasets
opendatasets.download(dataset_url)
`
Then, filter the dataset to get only potato data:
`
import shutil
import os
BASE_DIR = os.getcwd()
main_dir = '/content/plant-village/PlantVillage'
directories = os.listdir('/content/plant-village/PlantVillage')

dir_to_remove = []
for directory in directories:
  if not directory.startswith('Potato'):
    dir_to_remove.append(directory)

for dir in dir_to_remove:
  fullpath = os.path.join(main_dir,dir)
  shutil.rmtree(fullpath)

`
After that, split the dataset into training, validation, and testing sets using the following code:
`import splitfolders
splitfolders.ratio('/content/plant-village/PlantVillage',output='dataset',ratio =(.7,.1,.2) )

`










