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

![스크린샷 2023-10-16 오전 1 05 10](https://github.com/ZeC-bit/KYC-OCR-Project/assets/74304944/28679356-6e04-48a4-b9eb-0dcfc448bef3)

* Segmentation of text or not text, known as classification

* After the detection, print out the ROIs for TextBox and proceed with the Crop operation

**2.1 three types of detection CNN**
type1 pyramid + multi prediction (ssd)
pyramid + feature fusion + multi-prediction
pyramid + feature fusion + single prediction


## 3. Text Recognition

* Need to recognize what letters each image contains after cropping the image
* Composed of Convolution layer Model, and Recurrent layer Model
* Modules exist separately for each language of course / Can classify cropped textboxes by language


**3.1 Convolution Layer Model**
* It consists of three operations: convolutional, normalization, and maxpool
* Similar to Phase 2, shared CNNs are also available
* Split CNN images vertically, with multiple features for each letter
* Split features are also internally referred to as alignment


**3.2 Recurrent Layer Model**

* These alignments are learned through RNN
* Decoder exists to put the letters back together
* For decoder, CTC Loss(Connectionist temporal classification loss)
* Attachment is also available for decoder
![스크린샷 2023-10-16 오전 1 05 21](https://github.com/ZeC-bit/KYC-OCR-Project/assets/74304944/96f8f016-ad8a-48ef-81fc-303c205e6233)

## 4. Post-processing

* Throwing out low quality words
* Combining words to generate Sentence
* Supplement spelling check, etc. (ex. oat -> cat)




## 5. Open Source OCR Comparison

**Tesseract**
* Source Repository: https://github.com/tesseract-ocr/tesseract
* Open Source OCR tools with a relatively long history
* Google's developers maintain it after HP started developing it and turned it into an open source
* C-based development and multiple wrapper libraries are also abundant / offers a variety of options
* Weakness includes slow rate, GPU not supported


**EasyOCR**
* Source Repository: https://github.com/JaidedAI/EasyOCR
* Better accuracy than Tesseract
* Improved performance (speed) because it supports GPU operations
* Apache 2.0 for commercial use
* Ease of additional learning and enable additional font learning
* Using a text detection tool called CRAFT created and released by Naver


**ocr_kor**
* Source Repository: https://github.com/parksunwoo/ocr_kor
* OCR tool that learned Deep-text-recognition-benchmark in Korean, which was researched and released by Naver
* OCR in regular document fails because there is no text detection part
* Additional learning forms, such as providing a learning data generator

![스크린샷 2023-10-16 오전 1 05 43](https://github.com/ZeC-bit/KYC-OCR-Project/assets/74304944/12f95f55-4bf1-4ba1-841a-c91e78e84359)





