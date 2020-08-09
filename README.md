# Object-Detection_Opencv-Yolo
<br/>

### *The object detection model is tested on an image. We will test it on video stream soon...*

<br/>

Here you will learn how YOLO object detection algorithm is used to detect multimple objects and it's position in an image and video stream using opencv network.


<p align="centre">
  <img src="https://github.com/ArupDutta/Object-Detection_Opencv-Yolo/blob/master/output/imgg2.JPG">
</p>

We will start our discussion with Yolo. Let's be clear by saying that Yolo is a state-of-the-art, real-time object detection system(algorithm). On a Pascal Titan X it processes images at 30 FPS and has a mAP of 57.9% on COCO test-dev.


### How YOLO Works?
Prior detection systems uses classifiers or localizers to perform detection. They apply the model to an image at multiple locations and scales. High scoring regions of the image are considered as detections.
<br/>
<br/>
Yolo uses a totally different approach. It applies a single neural network to the full image. This network divides the image into regions and predicts bounding boxes and probabilities for each region. These bounding boxes are weighted by the predicted probabilities. 
<br/>
<br/>
The model has several advantages over classifier-based systems. It looks at the whole image at test time so its predictions are informed by global context in the image. It also makes predictions with a single network evaluation unlike systems like R-CNN which require thousands for a single image. This makes it extremely fast, more than 1000x faster than R-CNN and 100x faster than Fast R-CNN. See our paper for more details on the full system.
<br/>

We have two options to get started with object detection:
<br/>
1.  Using the pre-trained model<br/>
2.  Training custom object detector from scratch<br/>

*In this article, we will be looking at creating an object detector using the pre-trained Yolo model for images, videos and real-time webcam. Let us dive into the code.*


### How YOLO Detects Objects?
The 3 most used and known frameworks compatible with YOLO are -

*1. <b>Darknet:</b> It only works with Linux OS. It’s the framework built from the developer of YOLO and made specifically for yolo.* <br/>
*2. <b>Darkweb:</b> It uses darknet framework with tensorflow. This enables this framework to run on Linux, Windows and Mac OS* <br/>
*3. <b>Opencv:</b> It works on opencv. Make sure to have opencv==3.4.2 or more. This only workes with CPU but no extra installation is required.* <br/>



### How to Load YOLO Model using Opencv?
We will focus on how to use YOLO with Opencv. This is the easiest approach, to get quickly the algorythm working without doing complex installations. To load the algorithm we need 3 files. Follow [Instructions](https://github.com/ArupDutta/Object-Detection_Opencv-Yolo/blob/master/models/README.md)


<p align="centre">
  <img src="https://github.com/ArupDutta/Object-Detection_Opencv-Yolo/blob/master/output/imgg3.JPG">
</p>

### Detects Object - Write Code
Now that we have understood the functionality of YOLO and Opencv, we can download the project from [git repository](https://github.com/ArupDutta/Object-Detection_Opencv-Yolo) and start executing the [python script](https://github.com/ArupDutta/Object-Detection_Opencv-Yolo/blob/master/object_detection_image_yolo_opencv.ipynb). 
<br/>
<br/>
Like I mentioned before as well, our input can be in three forms:
1.  Image File
2.  Webcam Stream
3.  Video File

*Will come with the Webcamp stream and Video File code very soon*
