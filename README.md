# 😷 COVID-19 SOCIAL DISTANCING DETECTOR PROJECT
<p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/121768609-97a80700-cb91-11eb-86f2-968a503c4210.gif" width= "500" height= "500" align ="center" class="animated" />
</p>


## A. PROJECT SUMMARY

**Project Title:** Social Distancing Detector Project

**Team Members:** 

<p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/121847224-d3220d00-cd1a-11eb-82fb-6516c88c217f.png" width= "1000" height= "600" align ="center" class="animated" />
</p>

**Objectives:**
- To control the spread of contagious diseases - coronavirus.
- To act as an alternative to avoid drastic results in coronavirus disease.
- To reduce the physical contact between the infected and healthy people.

## B.  ABSTRACT 
Social distancing is a method used to control the spread of contagious diseases. It implies that people physically distance themselves from one another, reducing close contact, and thereby reducing the spread of a contagious disease (such as the COVID-19 Disease). In the battle against COVID-19, social distancing has proved to be a highly successful strategy for slowing the disease's spread. People are being urged to restrict their contacts with one another in order to reduce the risk of the virus spreading through physical or near contact. In the past, AI/Deep Learning has shown promise in solving a variety of everyday problems. We can see a clear overview of how we can use Python, Computer Vision, and Deep Learning to monitor social distancing in public places and workplaces in this proposed system. The social distancing detection tool will track whether people are maintaining a safe distance from each other in public places and the workplace to ensure social distancing protocol.

<p align="center">
  <img src="https://www.pyimagesearch.com/wp-content/uploads/2020/05/social_distance_detector_example.png" class="animated" />
</p>


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

Three python scripts will be reviewed:

- social_distancing_config.py: A Python file holding a number of constants in one convenient place.
- detection.py: YOLO object detection with OpenCV involves more lines of code that some easier models. We’ve decided to put the object detection logic in a function in this file for convenience. Doing so frees up our driver script’s frame processing loop from becoming especially cluttered
- social_distance_detector.py: This file is responsible for looping over frames of a video stream and ensuring that people are maintaining a healthy distance from one another during a pandemic. It is compatible with video files.

In the next two sections, we will train our social distancing detector.

## E. TRAINING THE SOCIAL DISTANCING DETECTOR

The model is trained by loading the dataset into the model first and then training it. The video stream is then identified once the model has been loaded. Finally, based on the distance frames, people are additionally labelled with markers indicating whether they maintain or violate social distancing.

![image](https://user-images.githubusercontent.com/74868126/121727464-8671e280-cb1e-11eb-8e0b-e094b2ac682e.png)

A video will be loaded as the input of Social Distancing Detector. People are classified as maintaining social distancing or not depending on how much gap they maintain between them. They'll be labelled with different coloured frames, and the number of people who aren't socially isolated will be displayed. When two or more individuals stand near to one another, the system detects no social distancing, calculates the total number of persons who breach social distance, and labels them with a red frame, but when the frame is blue, the system finds there is social distance.

![image](https://user-images.githubusercontent.com/74868126/121729429-0ac56500-cb21-11eb-8c55-e9d8adab609e.png)

### Output


## F.  RESULT AND CONCLUSION

### Result 📽️
<!-- <p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/120137446-eacfa080-c206-11eb-8d56-52484a170b04.gif" width= "1000" height= "600" align ="center" class="animated" />
</p>
 -->

### Conclusion
Our project distinguishes the social distancing pattern and classifies them as a violation of social distancing or maintaining the social distancing norm. Additionally, it also displays labels number of people who violate the social distancing through a video. However, this system can be implemented in CCTV for surveillance of people during pandemics. To restrict the spread of the Covid-19, social separation and other fundamental hygienic measures are now critical.



## G.  PROJECT PRESENTATION 
https://www.youtube.com/watch?v=9rfOVLf2wjs
