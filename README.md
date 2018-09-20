# Breast-Cancer-Image-Classification
### Classification of breast cancer images using CNNs.
1 in 8 US women will develop invasive breast cancer in their lifetime.
The lifetime risk of breast cancer for US men is 1 in 1000.

### PROBLEM
- Detecting the incidence and extent of cancer currently performed
by manually looking at images.
- Painstaking, long, inefficient and error-filled process.
### GOALS
- Train a model to classify images with invasive ductal carcinoma.

### Tech Stack
The following packages are used for the analysis:
pandas, numpy, keras, os, cv2 and matplotlib.

### Data cleaning
Data sourced from Kaggle, originally from research by Anant Madabhushi at Case Western. 50 patients (50166 images) are analyzed.
1. 162 whole mount slide color images. Each slide scanned at 40x zoom, broken down to 50x50 px images.
2. Each pixel is a 50x50 image (2D) encoded in red, green and blue.
3. The values are then normalized and converted to a 50x50x3 array (1D) where each pixel is a 3x1 vectorwith values ∈ S[0,1]. 

![alt text][logo]

[logo]: https://github.com/VNair88/Visualizing-the-Olympics/blob/master/Plots/summer_participation.JPG  "Summer participation"

### Basic model 
Output channels - 32
Maxpooling - pool size 2 x 2
Flattened layer
Dense layer - 100 nodes
Optimizer - sgd; Loss - crossentropy

### Final model 
4 convolution layers
Output channels: 32 & 64
Padding
Maxpooling - pool size 2 x 2
Dropout - 0.25
Dense layer - 512 nodes
Optimizer - Adadelta
Loss - crossentropy
Data augmentation

### Results
