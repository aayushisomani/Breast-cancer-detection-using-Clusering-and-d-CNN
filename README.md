# Breast-cancer-detection-using-Clusering-and-d-CNN

The dataset for this project can be downloaded from: https://www.kaggle.com/paultimothymooney/breast-histopathology-images

config.py: The TRAIN_SPLIT is the percentage of data that I used for training. Here I’ve set it to 80%, where the remaining 20% will be used for testing.
Of the training data, I have reserved some images for validation. Here, 10% of the training data (after we’ve split off the testing data) will be used for validation.

build_dataset.py: This script requires that we import  our config  settings and paths  for collecting all the image paths. We also will use random  to randomly shuffle our paths, shutil  to copy images, and os  for joining paths and making directories.

cancernet.py: To implement the d-CNN model I have used the Keras deep learning library and designed a network appropriately named “CancerNet” which:

-Uses exclusively 3×3 CONV filters, similar to VGGNet.

-Stacks multiple 3×3 CONV filters on top of each other prior to performing max-pooling (again, similar to VGGNet).

-But unlike VGGNet, uses depthwise separable convolution rather than standard convolution layers.
