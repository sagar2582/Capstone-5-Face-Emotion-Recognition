# Capstone-5-Face-Emotion-Recognition
A Deep Learning project to detect the Face Emotions.


----->>>>>>>>> INTRODUCTION

Emotion recognition is the process of identifying human emotion. People vary widely in their accuracy at recognizing the emotions of others. Use of technology to help people with emotion recognition is a relatively nascent research area. Generally, the technology works best if it uses multiple modalities in context. To date, the most work has been conducted on automating the recognition of facial expressions from video, spoken expressions from audio, written expressions from text, and physiology as measured by wearables.

Facial expressions are a form of nonverbal communication. Various studies have been done for the classification of these facial expressions. There is strong evidence for the universal facial expressions of seven emotions which include: neutral happy, sadness, anger, disgust, fear, and surprise. So it is very important to detect these emotions on the face as it has wide applications in the field of Computer Vision and Artificial Intelligence. These fields are researching on the facial emotions to get the sentiments of the humans automatically.

![image](https://user-images.githubusercontent.com/52121616/164030951-ddaebb34-a9d3-44b1-9059-a839d721e20f.png)



------->>>>>>> Problem statement

The Indian education landscape has been undergoing rapid changes for the past 10 years owing to the advancement of web-based learning services, specifically, eLearning platforms.

Global E-learning is estimated to witness an 8X over the next 5 years to reach USD 2B in 2021. India is expected to grow with a CAGR of 44% crossing the 10M users mark in 2021. Although the market is growing on a rapid scale, there are major challenges associated with digital learning when compared with brick and mortar classrooms. One of many challenges is how to ensure quality learning for students. Digital platforms might overpower physical classrooms in terms of content quality but when it comes to understanding whether students are able to grasp the content in a live class scenario is yet an open-end challenge. In a physical classroom during a lecturing teacher can see the faces and assess the emotion of the class and tune their lecture accordingly, whether he is going fast or slow. He can identify students who need special attention.

Digital classrooms are conducted via video telephony software program (ex-Zoom) where it’s not possible for medium scale class (25-50) to see all students and access the mood. Because of this drawback, students are not focusing on content due to lack of surveillance.

While digital platforms have limitations in terms of physical surveillance but it comes with the power of data and machines which can work for you. It provides data in the form of video, audio, and texts which can be analyzed using deep learning algorithms.

Deep learning backed system not only solves the surveillance issue, but it also removes the human bias from the system, and all information is no longer in the teacher’s brain rather translated in numbers that can be analyzed and tracked.

I will solve the above-mentioned challenge by applying deep learning algorithms to live video data. The solution to this problem is by recognizing facial emotions.



------>>>>>>  Dataset Information
The data comes from the past Kaggle competition “Challenges in Representation Learning: Facial Expression Recognition Challenge”. The faces have been automatically registered so that the face is more or less centered and occupies about the same amount of space in each image.

This dataset contains 35887 grayscale 48x48 pixel face images.

Each image corresponds to a facial expression in one of seven categories

Labels:

0 - Angry 😠

1 - Disgust 😧

2 - Fear 😨

3 - Happy 😃

4 - Sad 😞

5 - Surprise 😮

6 - Neutral 😐

Dataset link - https://www.kaggle.com/msambare/fer2013



------>>>>>> Dependencies

Python 3

Tensorflow 2.0

Streamlit

Streamlit-Webrtc

OpenCV


------>>>>>> Project Approach

Step 1. Build Model
We going to use three different models including pre-trained and Custom Models as follows:

   ->Method1: Using DeepFace
   ->Method2: Using ResNet
   ->Method3: Custom CNN Model
   
Step 2. Real Time Prediction
And then we perform Real Time Prediction on our best model using webcam on Google colab itself.

   ->Run webcam on Google Colab
   ->Load our best Model
   ->Real Time prediction
Step 3. Deployment
And lastly we will deploy it on two different plateform

   ->Streamlit Share
   ->Heroku
   
   
------>>>>>>>>> Method 1: Using DeepFace

Deepface is a lightweight face recognition and facial attribute analysis (age, gender, emotion and race) framework for python.

The process of facial recognition starts with the human face and identifying its necessary facial features and patterns. A human face comprises a very basic set of features, such as eyes, nose, and mouth. Facial recognition technology learns what a face is and how it looks. This is done by using deep neural network & machine learning algorithms on a set of images with human faces looking at different angles or positions.   


------>>>>>>>>> Method 2: Transfer Learning - Prediction Using ResNet50

Transfer learning (TL) is a research problem in machine learning (ML) that focuses on storing knowledge gained while solving one problem and applying it to a different but related problem. For example, knowledge gained while learning to recognize cars could apply when trying to recognize trucks. Reusing or transferring information from previously learned tasks to learning of new tasks has the potential to significantly improve the sample efficiency of a Data Scientist.

ResNet-50 is a convolutional neural network that is 50 layers deep. You can load a pretrained version of the network trained on more than a million images from the ImageNet database. The pretrained network can classify images into 1000 object categories, such as keyboard, mouse, pencil, and many animals.

![image](https://user-images.githubusercontent.com/52121616/164032869-006cc89d-66a8-47d6-8ced-25cb6a4d9298.png)


------->>>>>>>>> Method 3: Custom CNN Model

A convolution network generally consists of alternate convolution and max-pooling operations. The output obtained after applying convolution operation is shrunk using max-pooling operation which is then used as an input for the next layer.

A Convolutional Neural Network (ConvNet/CNN) is a Deep Learning algorithm which can take in an input image, assign importance (learnable weights and biases) to various aspects/objects in the image and be able to differentiate one from the other. The pre-processing required in a ConvNet is much lower as compared to other classification algorithms. While in primitive methods filters are hand-engineered, with enough training, ConvNets have the ability to learn these filters/characteristics. The architecture of a ConvNet is analogous to that of the connectivity pattern of Neurons in the Human Brain and was inspired by the organization of the Visual Cortex. Individual neurons respond to stimuli only in a restricted region of the visual field known as the Receptive Field. A collection of such fields overlap to cover the entire visual area.
![image](https://user-images.githubusercontent.com/52121616/164033128-cae61bfb-639d-41ee-bc33-02678d366066.png)

------->>>>>>>>>> Realtime Local Video Face Detection

The following photos and video contains the real time deploymnet of the app in local runtime
![image](https://user-images.githubusercontent.com/52121616/164033292-e74bd4d4-3770-4fbe-9f9a-2f8f506e8c7d.png)
![image](https://user-images.githubusercontent.com/52121616/164033333-0fadebca-ee02-4d7a-bd59-8abb0e2a8ae2.png)
![image](https://user-images.githubusercontent.com/52121616/164033356-45e3f544-9595-45a2-b864-987febe84fed.png)


------->>>>>>>>>> Deployment of Streamlit WebApp in Heroku and Streamlit

We have created front-end using Streamlit for webapp and used streamlit-webrtc which helped to deal with real-time video streams. Image captured from the webcam is sent to VideoTransformer function to detect the emotion. Then this model was deployed on heroku platform with the help of buildpack-apt which is necessary to deploy opencv model on heroku.

