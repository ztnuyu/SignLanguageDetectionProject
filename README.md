# 😷 COVID-19 SOCIAL DISTANCING DETECTOR PROJECT

## A. PROJECT SUMMARY

**Project Title:** Social Distancing Detector Project

**Team Members:** 
- Nur Aisah Tan binti Osman Tan - B031920006
- Fatin Najiha binti Mohd Tarmidi - B031920036
- Nurul Izzati binti Suhaimi - B031920001
- Wan Mohamad Nur'Akid Bin Wan Muhammad


**Objectives:**
- To control the spread of contagious diseases - coronavirus.
- To act as an alternative to avoid drastic results in coronavirus disease.
- To reduce the physical contact between the infected and healthy people.

## B.  ABSTRACT 
Social distancing is a method used to control the spread of contagious diseases. It implies that people physically distance themselves from one another, reducing close contact, and thereby reducing the spread of a contagious disease (such as the COVID-19 Disease). In the battle against COVID-19, social distancing has proved to be a highly successful strategy for slowing the disease's spread. People are being urged to restrict their contacts with one another in order to reduce the risk of the virus spreading through physical or near contact. In the past, AI/Deep Learning has shown promise in solving a variety of everyday problems. We can see a clear overview of how we can use Python, Computer Vision, and Deep Learning to monitor social distancing in public places and workplaces in this proposed system. The social distancing detection tool will track whether people are maintaining a safe distance from each other in public places and the workplace to ensure social distancing protocol.

![Coding](https://www.pyimagesearch.com/wp-content/uploads/2020/05/social_distance_detector_example.png)

Figure 1: Social distancing is important in times of epidemics and pandemics to prevent the spread of disease.

## C.  DATASET

## D.  PROJECT STRUCTURE

The following directory is our structure of our project:

- $ tree --dirsfirst --filelimit 10
- .
- ├── pyimagesearch
- │   ├── __init__.py
- |   ├── detection.py
- │   └── social_distancing_config.py
- ├── yolo-coco
- │   ├── coco.names
- │   ├── yolov3.cfg
- │   └── yolov3.weights
- ├── output.avi
- ├── pedestrians.mp4
- └── social_distance_detector.py
- 2 directories, 9 files

Our YOLO object detector files including the CNN architecture definition, pre-trained weights, and class names are housed in the yolo-coco/ directory. This YOLO model is compatible with OpenCV’s DNN module.

We’ll be reviewing three Python scripts in this tutorial:

- social_distancing_config.py: A Python file holding a number of constants in one convenient place.
- detection.py: YOLO object detection with OpenCV involves more lines of code that some easier models. We’ve decided to put the object detection logic in a function in this file for convenience. Doing so frees up our driver script’s frame processing loop from becoming especially cluttered
- social_distance_detector.py: This file is responsible for looping over frames of a video stream and ensuring that people are maintaining a healthy distance from one another during a pandemic. It is compatible with video files.

In the next two sections, we will train our social distancing detector.

## E   TRAINING THE SOCIAL DISTANCING DETECTOR



## F.  RESULT AND CONCLUSION

### Demo 📽️


![60b45f6b3c061900409088](https://user-images.githubusercontent.com/73053555/120137932-f7a0c400-c207-11eb-8e3a-c714fbb4adb8.gif)


### Result 📽️

![60b45dab77bff301509658](https://user-images.githubusercontent.com/73053555/120137446-eacfa080-c206-11eb-8d56-52484a170b04.gif)





## G.  PROJECT PRESENTATION 

