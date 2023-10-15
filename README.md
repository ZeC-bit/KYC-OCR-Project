# KYC-OCR-Project

OCR is Optical Character Recognition which is deep learning framework to recognize the optical characters.




## 4 Process of OCR 
 
+ Step 1 (Pre-processing)  
+ Step 2 (Text Detection)  
+ Step 3 (Text recognition)  
+ Step 4 (Post-processing)  


![스크린샷 2023-10-16 오전 12 46 45](https://github.com/ZeC-bit/KYC-OCR-Project/assets/74304944/d0015666-0e2c-41fb-8c88-f8b9fa2cb07c)

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

![스크린샷 2023-10-16 오전 12 46 45](https://github.com/ZeC-bit/KYC-OCR-Project/assets/74304944/d0015666-0e2c-41fb-8c88-f8b9fa2cb07c)
![스크린샷 2023-10-16 오전 1 05 43](https://github.com/ZeC-bit/KYC-OCR-Project/assets/74304944/12f95f55-4bf1-4ba1-841a-c91e78e84359)
![스크린샷 2023-10-16 오전 1 05 10](https://github.com/ZeC-bit/KYC-OCR-Project/assets/74304944/28679356-6e04-48a4-b9eb-0dcfc448bef3)
![스크린샷 2023-10-16 오전 1 05 21](https://github.com/ZeC-bit/KYC-OCR-Project/assets/74304944/96f8f016-ad8a-48ef-81fc-303c205e6233)







