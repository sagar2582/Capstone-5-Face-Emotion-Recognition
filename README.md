# Capstone-5-Face-Emotion-Recognition
A Deep Learning project to detect the Face Emotions.


----->>>>>>>>> INTRODUCTION

Emotion recognition is the process of identifying human emotion. People vary widely in their accuracy at recognizing the emotions of others. Use of technology to help people with emotion recognition is a relatively nascent research area. Generally, the technology works best if it uses multiple modalities in context. To date, the most work has been conducted on automating the recognition of facial expressions from video, spoken expressions from audio, written expressions from text, and physiology as measured by wearables.

Facial expressions are a form of nonverbal communication. Various studies have been done for the classification of these facial expressions. There is strong evidence for the universal facial expressions of seven emotions which include: neutral happy, sadness, anger, disgust, fear, and surprise. So it is very important to detect these emotions on the face as it has wide applications in the field of Computer Vision and Artificial Intelligence. These fields are researching on the facial emotions to get the sentiments of the humans automatically.

![image](https://user-images.githubusercontent.com/52121616/164030951-ddaebb34-a9d3-44b1-9059-a839d721e20f.png)



------->>>>>>> Problem statement

We will solve the above-mentioned challenge by applying deep learning algorithms to live video data. The solution to this problem is by recognizing facial emotions.
->Face Emotion Recognition:
This is a few shot learning live face emotion detection system. The model should be able to real-time identify the emotions of students in a live class.



----->>>>>1.3 Scope of Project
A. Model should be able to identify students’ emotions using minimum reference images.

B. Model should work on the real-time webcam video feed.

C. Model must be deployed on AWS/GCP/Azure platform as an end-to-end solution.

D. Model must be accessible via a web application (Streamlit) for demo purposes.





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
