Question/need:
- What is the framing question of your analysis, or the purpose of the model/system you plan to build?  
	- Ultrasound of the heart, known as echocardiography, is a widely used technique for assessing heart function and structure. Currently, interpretation of an echocardiogram is performed by a highly trained human, but even the most skilled of these humans are not always accurate. Therefore, there is an opportunity for deep learning to improve the reliability and accuracy of echocardiogram interpretation in general -  and to potentially make it possible for a less skilled human to interpret this test. The goal of this project is to apply a deep learning model to echocardiogram video clips in order to predict the ejection fraction, a central metric of cardiac function. 

- Who benefits from exploring this question or building this model/system?
	- Increasing the reliability and accuracy of echocardiogram interpretation ultimately benefits the patients who need this test. 

Data Description:
- What dataset(s) do you plan to use, and how will you obtain the data?
	- I plan to use the EchoNet-Dynamic Dataset, which contains 10,036 gray-scale echocardiography videos, each from a single patient. Each video captures the same view of the heart: an apical-4-chamber view. Each video is accompanied by human expert tracings of the left ventricle at end-systolic volume (ESV) and end-diastolic volume (EDV), as well as measurements of ESV, EDV and ejection fraction. I plan to obtain the dataset via download. It was published in the following paper:  
		- Ouyang, David et al. “EchoNet-Dynamic: a Large New Cardiac Motion Video Data Resource for Medical Machine Learning.” (2019).

- What is an individual sample/unit of analysis in this project? What characteristics/features do you expect to work with?
	- An individual unit of analysis is a single echocardiography video. As mentioned above, each video features the apical-4-chamber view. In the standard echocardiogram workflow, a human expert uses this view to trace the size of the left ventricle (largest of the 4 chambers) at 2 time points: end-systole (maximum contraction - occurs when the chamber is at minimum size) and end-diastole (maximum relaxation - occurs when the chamber is at maximum size). The tracings are then used to calculate the two volumes (EDV and ESV), and these are used to calculate the ejection fraction. I will need to train the model to measure these two volumes, and then use them to calculate the ejection fraction.
- If modeling, what will you predict as your target? 
	- The target I will be predicting is the ejection fraction


Tools:
- How do you intend to meet the tools requirement of the project?
	- I will use python neural network tools, likely a Convolutional Neural Network (CNN) along with a Recurrent Neural Network (RNN) (CNN-RNN)
- Are you planning in advance to need or use additional tools beyond those required? 
	- I plan to use Google co-lab for cloud computing and OpenCV’s VideoCapture method to read frames from videos

MVP Goal:
- What would a minimum viable product (MVP) look like for this project?
	- A MVP would be a CNN-RNN model 
