# Face Detector with JavaScript in the browser
The main goal of this project is to implement a web app face detector. The web app will receive an image from the user and display the name of each person.
In order to implement a face detector, I am going to use the face-api.js.

## What you must learn before start this project
1. Promisses,
2. Async
3. Canva
4. setInterval and setTimeout

## About Face-api.js

It is a JavaScript face recognition API for the browser and nodejs implemented on top of tensorflow.js core

Link:

https://github.com/justadudewhohacks/face-api.js

### Features
1. Face Recognition
2. Face Landmark Detection
3. Face Expression Recognition
4. Age Estimation & Gender Recognition

# How to implement this project
1. Include the latest script from the following link in your index.html page

https://github.com/justadudewhohacks/face-api.js/tree/master/dist


2. Set the video tag
    2.1. The video tag has no source attribute because the source is going to be set via JavaScript. 
    2.2. Include autoplay and muted
    3.3 Set an id, that is going to be uset to get the element on the script.
    3.4 Set the width and height

    ```
 <video id="video" width="720" height="560" autoplay muted></video>
 ```

3. Loading the models
All instances are exported via faceapi.nets:
```
faceapi.nets.tinyFaceDetector.loadFromUri('/scripts/models'),
faceapi.nets.faceLandmark68Net.loadFromUri('/scripts/models'),
faceapi.nets.faceRecognitionNet.loadFromUri('/scripts/models'),
faceapi.nets.faceExpressionNet.loadFromUri('/scripts/models'),
faceapi.nets.ageGenderNet.loadFromUri('/scripts/models'),
faceapi.nets.ssdMobilenetv1.loadFromUri('/scripts/models')
```
You can consult all names:
```
console.log(faceapi.nets)
// ageGenderNet
// faceLandmark68Net
// faceRecognitionNet

// tinyFaceDetector
// tinyYolov2
```

You can check the description of all models on the following link
https://github.com/justadudewhohacks/face-api.js#available-models



