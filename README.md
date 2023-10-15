# KYC-OCR-Project

OCR is Optical Character Recognition which is deep learning framework to recognize the optical characters.




## 4 Process of OCR 

+ Step 1 (Pre-processing)  
+ Step 2 (Text Detection)  
+ Step 3 (Text recognition)  
+ Step 4 (Post-processing)  



**Accuracy, Recall Value of RNN** 

## 1. Preprocessing

* In the process of processing documents digitally, noise and distortion often lead to significantly lower recognition rates. => Can improve recognition rate through preprocessing
* Grayscale conversion
* Histogram normalization
* Redistribute the distribution of brightness to maximize contrast for clearer images


## 2. Text Detection


* Select text areas from images to reduce unnecessary calculations
* FeatureMap extraction with Convolution
* rotation angle regression



* Segmentation of text or not text, known as classification

* After the detection, print out the ROIs for TextBox and proceed with the Crop operation







