# Indoor/Outdoor Security System (Deployement using C++)

Goal of this project is deployment of security system for detection of human for indoor/outdoor.

The final product is an embedded system equipped with camera that in real-time gives alarm in the case of seeing human. 
This project has three main steps: 
In the first step, I implemented the SSD object detection which is finetuned for new dataset. 
In the second step, I deploy the inference part on server using C++.
In the third step, I deploy the inference part on embedded system (Dragon board 410C) using C++.


# 1. Training & Fine tuning of Model 
In this step, I finetuned the SSD Mobilenet_V1 to be used for deployment. 
For details of this step please refer to https://github.com/KhosroBahrami/ObjectDetection_SSD_Tensorflow.




# 2.Deployment on Server
To deploy SSD object detection on server, I did/prepared the following steps:

### Software requirements:
- Installation of Debian linux
- Installation of Bazel (to compile tensorflow)
- Installation of Tensorflow
- Installation of OpenCV
- The object detection code

### Pipeline of our system includes the following steps:

- Capture the live video from camera
- Extract the images/frames from the input video
- Resize every image/frame for the SSD network
- Run the SSD network on the resized image/frame
- Apply the Non-Maximum Suppression algorithm to get rid of multiple detections of a single object
- Display the frames with the bounding box of detected objects.




# 3.Deployment on DragonBoard 410c
To deploy SSD object detection on the DragonBoard 410c, I did/prepared the following steps:

### Hardware requirements:
- Using a DragonBoard 410c, USB camera, keyboard, mouse, HDMI monitor.
- Using a 16GB MicroSD Card
- Partition the 16GB MicroSD card into 4GB and 12GB.
- The 4GB of SD card was used to increase the memory (DragonBoard 410c has 1GB memory).
- The 12GB of SD card was used to increase the storage (DragonBoard 410c has 8GB storage).

### Software requirements:
- Installation of Debian linux
- Installation of Bazel (to compile tensorflow)
- Installation of Tensorflow
- Installation of OpenCV
- The object detection code
- Pipeline of our system for pedestrain detection

### The pipeline of our system includes the following steps:

- Capture the live video from camera
- Extract the images/frames from the input video
- Resize every image/frame for the SSD network
- Run the SSD network on the resized image/frame
- Apply the Non-Maximum Suppression algorithm to get rid of multiple detections of a single object
- Display the frames with the bounding box of detected objects.

