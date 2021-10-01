Abstract

The goal of this project is to apply a deep learning model to echocardiogram images in order to classify the images by their timing in the cardiac cycle: end-diastole (max relaxation), end-systole (max contraction), or neither. I used the EchoNet-Dynamic Dataset, which contains 10,036 gray-scale echocardiography videos. I trained a series of simple CNNs with 5 layers. My final model scores an accuracy of 0.743. The model excels at distinguishing end-systole from end-diastole and vice versa. But the model struggles to classify the “Other” class. 

Design
The goal of this project is to apply a deep learning model to echocardiogram images in order to classify the images by their timing in the cardiac cycle: end-diastole (max relaxation), end-systole (max contraction), or neither. 

Data
I used the EchoNet-Dynamic Dataset, which contains 10,036 gray-scale echocardiography videos, each from a single patient. Each video captures the same view of the heart: an apical-4-chamber view. I obtained the dataset via download. It was published in the following paper:  
Ouyang, David et al. “EchoNet-Dynamic: a Large New Cardiac Motion Video Data Resource for Medical Machine Learning.” (2019).
I converted the videos into individual frames and extracted 3 images per video based on their timing in the cardiac cycle: end-diastole (max relaxation), end-systole (max contraction), or neither.

Algorithms
I trained a series of simple CNNs with 5 layers. My final model scores an accuracy of 0.743.
- The model excels at distinguishing end-systole from end-diastole and vice versa. But the model struggles to classify the “Other” class. This makes sense because this class contains more varied images

Tools
I used Google co-lab for cloud computing and OpenCV’s VideoCapture method to read frames from videos

Communication
Looking forward to the presentation!
