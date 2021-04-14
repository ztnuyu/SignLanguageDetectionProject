
# REAL TIME SIGN LANGUAGE DETECTION

## A. PROJECT SUMMARY

**Project Title:** Real Time Sign Language Detection

**Team Members:** 
- Nur Aisah Tan binti Osman Tan
- Fatin Najiha binti Mohd Tarmidi
- Nurul Izzati binti Suhaimi
- Wan Mohamad Nur'Akid Bin Wan Muhammad


**Objectives:**
- to bridge the gap of speech between hearing impaired people and the normal people
- to build a machine learning model that will be able to classify the various hand gestures used in sign language
- to present a real time system of sign language detection.


##  B. ABSTRACT 

Deaf and mute people are usually deprived of normal communication with other people in the society. Also normal people find it difficult to understand and communicate with them. These people have to rely on an interpreter or on some sort of visual communication. An interpreter won’t be always available and visual communication is mostly difficult to understand. Sign Language is the primary means of communication in the deaf and dumb community. As a normal person is unaware of the grammar or meaning of various gestures that are part of a sign language, it is primarily limited to their families and/or deaf and dumb community.

The only way the speech and hearing impaired (i.e deaf) people can communicate is by sign language. The main problem of this way of communication is normal people who cannot understand sign language can’t communicate with these people or vice versa. Our project aims to bridge the gap between the speech and hearing impaired people and the normal people. The basic idea of this project is to make a system using which deaf people can significantly communicate with all other people using their normal gestures. The system does not require the background to be perfectly black. It works on any background. The project uses image processing system to identify, especially basic sign language gesture used by the deaf people to communicate and converts them into text so that normal people can understand.

## C.  DATASET

In this project, we’ll discuss our two-phase COVID-19 face mask detector, detailing how our computer vision/deep learning pipeline will be implemented.

From there, we’ll review the dataset we’ll be using to train our custom face mask detector.

I’ll then show you how to implement a Python script to train a face mask detector on our dataset using Keras and TensorFlow.

We’ll use this Python script to train a face mask detector and review the results.

Given the trained COVID-19 face mask detector, we’ll proceed to implement two more additional Python scripts used to:

- Detect COVID-19 face masks in images
- Detect face masks in real-time video streams

We’ll wrap up the post by looking at the results of applying our face mask detector.


There is two-phase COVID-19 face mask detector as shown in Figure 2:

![Figure 2](https://www.pyimagesearch.com/wp-content/uploads/2020/04/face_mask_detection_phases.png)
Figure 2: Phases and individual steps for building a COVID-19 face mask detector with computer vision and deep learning 

In order to train a custom face mask detector, we need to break our project into two distinct phases, each with its own respective sub-steps (as shown by Figure 1 above):

- Training: Here we’ll focus on loading our face mask detection dataset from disk, training a model (using Keras/TensorFlow) on this dataset, and then serializing the face mask detector to disk

- Deployment: Once the face mask detector is trained, we can then move on to loading the mask detector, performing face detection, and then classifying each face as with_mask or without_mask

We’ll review each of these phases and associated subsets in detail in the remainder of this tutorial, but in the meantime, let’s take a look at the dataset we’ll be using to train our COVID-19 face mask detector.


Our COVID-19 face mask detection dataset as shown in Figure 3:

![Figure 3](https://www.pyimagesearch.com/wp-content/uploads/2020/04/face_mask_detection_dataset.jpg)

Figure 3: A face mask detection dataset consists of “with mask” and “without mask” images. 

The dataset we’ll be using here today was created by PyImageSearch reader Prajna Bhandary.

This dataset consists of 1,376 images belonging to two classes:

- with_mask: 690 images
- without_mask: 686 images

Our goal is to train a custom deep learning model to detect whether a person is or is not wearing a mask.

How was our face mask dataset created?
Prajna, like me, has been feeling down and depressed about the state of the world — thousands of people are dying each day, and for many of us, there is very little (if anything) we can do.

To help keep her spirits up, Prajna decided to distract herself by applying computer vision and deep learning to solve a real-world problem:

- Best case scenario — she could use her project to help others
- Worst case scenario — it gave her a much needed mental escape


## D.   PROJECT STRUCTURE



## E   TRAINING THE REAL TIME SIGN LANGUAGE DETECTION



## F.  RESULT AND CONCLUSION



## G.   PROJECT PRESENTATION 




