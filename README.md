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

<p align="center">Figure 1: Social distancing is important in times of epidemics and pandemics to prevent the spread of disease.</p>

The Yolo algorithm stands for You Only Look Once, this algorithm is a state of art, which works on a real-time system, build on deep learning for solving various Object Detection as well as Object Tracking problems. The architecture of Yolo can be observed from the below Figure 2.

<p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/121987569-51d68300-cdcb-11eb-85dc-2b6e65ecfd14.png" class="animated" />
</p>

<p align="center">Figure 2: YOLO Architecture- Image</p>

The architecture can be seen in the above diagram to contain the Input image layers, which are responsible for receiving the inputs that will be transmitted to subsequent levels. The input can be any picture depending on the use cases. Along the input layer is the DarkNet Architecture, which is an open-source neural network framework built with C and CUDA. This framework includes YOLO for object identification and tracking.


## C.  DATASET

We use 4 videos with different environment as our dataset for training our social distancing detector. 

<p align="center">Video 1</>
<p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/122071224-27b3ae00-ce29-11eb-9061-2ca9239e37b7.gif" width= "500" height= "250" align ="center" class="animated" /></p>
<p align="center"> This video was taken from Kolej Kediaman Satria, UTeM on 14th May 2021 by our group member. </>


<p align="center">Video 2</>
<p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/121910989-ee643b00-cd61-11eb-82e9-d587ad53b654.gif" width= "500" height= "250" align ="center" class="animated" /></p>
<p align="center"> This video was taken from KFC, Alor Setar Kedah on 14th May 2021 by our group member. </>


<p align="center">Video 3</>
<p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/121914753-2456ee80-cd65-11eb-8f1c-4ecfa2a2c881.gif" width= "500" height= "250" align ="center" class="animated" />
</p>
<p align="center"> This video was taken from Petaling Street Chinatown, Kuala Lumpur by a youtuber.</>

  
<p align="center">Video 4</>
<p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/121911140-10f65400-cd62-11eb-8c23-9fd287aac259.gif" width= "500" height= "250" align ="center" class="animated" />
</p>
<p align="center"> This video was taken from Zoo Melaka in Melaka. Our source of this video is from Youtube. </>



## D.  PROJECT STRUCTURE

The following directory is our structure of our project:

- $ tree --dirsfirst --filelimit 10
- .
- ├── result
- │   ├── outputkfc.avi
- |   ├── outputkl.avi
- |   ├── outpututem.avi  
- │   └── outputzoo.avi
- ├── src
- │   ├── config.py
- │   ├── detection.py
- │   └── social_distancing_detector.py
- ├── yolo-object-detector-algorithm
- │   ├── coco.names
- │   └── yolov4.cfg
- 3 directories, 9 files

Our YOLO object detector files including the CNN architecture definition, pre-trained weights, and class names are housed in the yolo-object-detector-algorithm/ directory. This YOLO model is compatible with OpenCV’s DNN module.

Three python scripts will be reviewed:

- config.py: A Python file holding a number of constants in one convenient place.
- detection.py: YOLO object detection with OpenCV involves more lines of code that some easier models. We’ve decided to put the object detection logic in a function in this file for convenience. Doing so frees up our driver script’s frame processing loop from becoming especially cluttered
- social_distance_detector.py: This file is responsible for looping over frames of a video stream and ensuring that people are maintaining a healthy distance from one another during a pandemic. It is compatible with video files.

In the next two sections, we will train our social distancing detector.

## E. TRAINING THE SOCIAL DISTANCING DETECTOR

The model is trained by loading the dataset into the model first and then training it. The video stream is then identified once the model has been loaded. Finally, based on the distance frames, people are additionally labelled with markers indicating whether they maintain or violate social distancing.

![image](https://user-images.githubusercontent.com/74868126/121727464-8671e280-cb1e-11eb-8e0b-e094b2ac682e.png)

A video will be loaded as the input of Social Distancing Detector. People are classified as maintaining social distancing or not depending on how much gap they maintain between them. They'll be labelled with different coloured frames, and the number of people who aren't socially isolated will be displayed. When two or more individuals stand near to one another, the system detects no social distancing, calculates the total number of persons who breach social distance, and labels them with a red frame, but when the frame is blue, the system finds there is social distance.

![image](https://user-images.githubusercontent.com/74868126/121729429-0ac56500-cb21-11eb-8c55-e9d8adab609e.png)

### Train Model
```
Epoch 1/35
938/938 [==============================] - 3s 3ms/step - loss: 0.4440 - accuracy: 0.8425
Epoch 2/35
938/938 [==============================] - 2s 2ms/step - loss: 0.4273 - accuracy: 0.8474
Epoch 3/35
938/938 [==============================] - 2s 2ms/step - loss: 0.4149 - accuracy: 0.8498
Epoch 4/35
938/938 [==============================] - 2s 2ms/step - loss: 0.4046 - accuracy: 0.8534
Epoch 5/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3961 - accuracy: 0.8548
Epoch 6/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3894 - accuracy: 0.8586
Epoch 7/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3836 - accuracy: 0.8607
Epoch 8/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3795 - accuracy: 0.8610
Epoch 9/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3742 - accuracy: 0.8622
Epoch 10/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3713 - accuracy: 0.8641
Epoch 11/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3650 - accuracy: 0.8659
Epoch 12/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3620 - accuracy: 0.8668
Epoch 13/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3589 - accuracy: 0.8673
Epoch 14/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3542 - accuracy: 0.8691
Epoch 15/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3534 - accuracy: 0.8680
Epoch 16/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3512 - accuracy: 0.8685
Epoch 17/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3469 - accuracy: 0.8720
Epoch 18/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3446 - accuracy: 0.8724
Epoch 19/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3445 - accuracy: 0.8731
Epoch 20/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3408 - accuracy: 0.8736
Epoch 21/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3402 - accuracy: 0.8730
Epoch 22/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3381 - accuracy: 0.8734
Epoch 23/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3345 - accuracy: 0.8748
Epoch 24/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3340 - accuracy: 0.8742
Epoch 25/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3324 - accuracy: 0.8760
Epoch 26/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3281 - accuracy: 0.8765
Epoch 27/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3284 - accuracy: 0.8765
Epoch 28/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3271 - accuracy: 0.8783
Epoch 29/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3276 - accuracy: 0.8773
Epoch 30/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3274 - accuracy: 0.8759
Epoch 31/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3236 - accuracy: 0.8793
Epoch 32/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3230 - accuracy: 0.8783
Epoch 33/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3214 - accuracy: 0.8799
Epoch 34/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3170 - accuracy: 0.8800
Epoch 35/35
938/938 [==============================] - 2s 2ms/step - loss: 0.3181 - accuracy: 0.8807
<tensorflow.python.keras.callbacks.History at 0x7f5e06d97fd0>
```

### Plotting Accuracy and Loss

![image](https://user-images.githubusercontent.com/74868126/122054465-48c0d280-ce1a-11eb-8224-ba3ebe43ae99.png)
![image](https://user-images.githubusercontent.com/74868126/122054498-50807700-ce1a-11eb-96bb-823d0d97bae7.png)

Here we use Tensorboard in Google Colaboratory.
From the plot of accuracy and loss we can see that the model showing comparable skill on the train and validation datasets. The gap between training and validation accuracy has a little overfitting. 


## F.  RESULT AND CONCLUSION

The experimental results section for this project details the results obtained after doing various observations and forming final outputs. This project focuses on social distancing detection for the events of Covid-19, Figure 3 explains the architecture for calculating the distance between objects and shows the flow of how the output is getting generated with the use of Yolo Version 4.

<p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/121987903-f789f200-cdcb-11eb-979a-80799a2ded35.png" width= "500" height= "250" align ="center" class="animated" />
</p>

<p align="center">Figure 3: YOLO Darknet Architecture</p>

### Result 📽️
<!-- <p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/121910989-ee643b00-cd61-11eb-82e9-d587ad53b654.gif" width= "500" height= "250" align ="center" class="animated" />
</p> -->

<p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/121911088-02a83800-cd62-11eb-8b68-e00a4881330b.gif" width= "500" height= "250" align ="center" class="animated" />
</p>
<p align="center">Result 1: Result in KFC Restaurant in Kedah</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/122016067-44cd8a00-cdf3-11eb-9fc8-e37497111e2e.gif" width= "500" height= "250" align ="center" class="animated" />
</p>
<p align="center">Result 4: Result in UTeM Satria</p>

<!-- <p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/121911140-10f65400-cd62-11eb-8c23-9fd287aac259.gif" width= "500" height= "250" align ="center" class="animated" />
</p> -->

<p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/121913946-67649200-cd64-11eb-8871-a625d30a7c00.gif" width= "500" height= "250" align ="center" class="animated" />
</p>
<p align="center">Result 2: Result in Zoo Melaka</p>

<!-- <p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/121914753-2456ee80-cd65-11eb-8f1c-4ecfa2a2c881.gif" width= "500" height= "250" align ="center" class="animated" />
</p> -->

<p align="center">
  <img src="https://user-images.githubusercontent.com/73053555/121914256-ae528780-cd64-11eb-854a-e1fc4450cc14.gif" width= "500" height= "250" align ="center" class="animated" />
</p>
<p align="center">Result 3: Result in KL Streets</p>



### Conclusion
Our project distinguishes the social distancing pattern and classifies them as a violation of social distancing or maintaining the social distancing norm. Additionally, it also displays labels number of people who violate the social distancing through a video. However, this system can be implemented in CCTV for surveillance of people during pandemics. To restrict the spread of the Covid-19, social separation and other fundamental hygienic measures are now critical.



## G.  PROJECT PRESENTATION 

In this project, we have learned how to implement a social distancing detector using OpenCV, computer vision, and deep learning.

Our implementation worked by:

- Using the YOLO object detector to detect people in a video stream ✔️
 - Determining the centroids for each detected person ✔️
 - Computing the pairwise distances between all centroids ✔️
 - Checking to see if any pairwise distances were < N pixels apart, and if so, indicating that the pair of people violated social distancing rules ✔️
<p>
  Furthermore, by using an NVIDIA CUDA-capable GPU, along with OpenCV’s dnn module compiled with NVIDIA GPU support, our method was able to run in real-time, making it usable as a proof-of-concept social distancing detector.
</p>

[![livedemo](https://user-images.githubusercontent.com/74868126/122067466-2e8cf180-ce26-11eb-8665-f17553d2dd54.png)](https://www.youtube.com/watch?v=4M2os8F2-OA "DEMO")

<p><a href="https://www.youtube.com/watch?v=4M2os8F2-OA">Click here to proceed with project demo</a></p>


## H. ACKNOWLEDGEMENT

### Sources that our group consults from:

### Source Code and Information
<p>:point_right:<a href="https://www.pyimagesearch.com/2020/06/01/opencv-social-distancing-detector/">Social Distancing Detector</a></p>
<p>:point_right:<a href="https://drive.google.com/drive/folders/1o2FcVhLI3uJYfrcD9mPyTR3EZjgulZKY">Open Source Code Google Drive</a></p>
<p>:point_right:<a href="https://www.youtube.com/watch?v=eBlRTel6AJY&t=3s">Youtube Video on Social Distancing Detector</a></p>


### Videos for Dataset and Training
<p>:point_right:<a href="https://www.youtube.com/watch?v=ar3JK0Qbxmw">Dinosaur Encounter @ Zoo Melaka, Melaka, Malaysia</a></p>
<p>:point_right:<a href="https://www.youtube.com/watch?v=XSubEn_d_gc&t=133s">Kwai Chai Hong, Petaling Street Chinatown, Kuala Lumpur, Malaysia</a></p>



