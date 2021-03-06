# Breast-Cancer-Image-Classification 
Data sourced from - https://www.kaggle.com/paultimothymooney/predicting-idc-in-breast-cancer-histology-images/data

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
Data sourced from Kaggle, originally from research by Anant Madabhushi at Case Western contains information about 50 patients (50166 images). For the purposes of this analysis, models are trained on 10,000 images and tested on 3000 images.
1. 162 whole mount slide color images. Each slide scanned at 40x zoom, broken down to 50x50 px images. 
2. Each pixel is a 50x50 image (2D) encoded in red, green and blue.
3. The values are then normalized and converted to a 50x50x3 array (1D) where each pixel is a 3x1 vectorwith values ∈ S[0,1]. 

![alt text][logo]

[logo]: https://github.com/VNair88/Breast-Cancer-Image-Classification/blob/master/Images/Capture.JPG  "Image rendition"

### Basic model 
Output channels - 32 <br>
Maxpooling - pool size 2 x 2 <br>
Flattened layer <br>
Dense layer - 100 nodes <br>
Optimizer - sgd; Loss - crossentropy 

### Final model 
4 convolution layers <br>
Output channels: 32 & 64 <br>
Padding <br>
Maxpooling - pool size 2 x 2 <br>
Dropout - 0.25 <br> 
Dense layer - 512 nodes <br>
Optimizer - RMS <br>
Loss - crossentropy <br>
Data augmentation

### Results
86% accuracy over 10 Epochs 

Confusion matrix - 

![alt text][logo1]

[logo1]: https://github.com/VNair88/Breast-Cancer-Image-Classification/blob/master/Images/Capture2.JPG  "Confusion matrix"
