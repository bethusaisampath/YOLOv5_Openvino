# Object Detection & YOLOs
Object detection is a technique of training computers to detect objects from images or videos. Over the years, there are many object detection architectures and algorithms created by multiple companies and researchers.

YOLO refers to “You Only Look Once” is one of the most versatile and famous object detection models. For every real-time object detection work, YOLO is the first choice by Data Scientist and Machine learning engineers. YOLO algorithms divide all the given input images into the SxS grid system. Each grid is responsible for object detection. Now those Grid cells predict the boundary boxes for the detected object. For every box, we have five main attributes: x and y for coordinates, w and h for width and height of the object, and a confidence score for the probability that the box containing the object.

The YOLO network consists of three main pieces-
1) Backbone - A convolutional neural network that aggregates and forms image features at different granularities.

2) Neck - A series of layers to mix and combine image features to pass them forward to prediction.

3) Head - Consumes features from the neck and takes box and class prediction steps.

## YOLOv5
After a few days of the release of the YOLOv4 model on 27 May 2020, YOLOv5 got released by [Glenn Jocher](https://www.linkedin.com/in/glenn-jocher/)(Founder & CEO of Utralytics). It was publicly released on Github [here](https://github.com/ultralytics/yolov5). Glenn introduced the YOLOv5 Pytorch based approach, and Yes! YOLOv5 is written in the Pytorch framework.

It is state of the art and newest version of the YOLO object detection series, and with the continuous effort and 58 open source contributors, YOLOv5 set the benchmark for object detection models very high; as shown below, it already beats the EfficientDet and its other previous YOLOv5 versions.
# YOLOv5 Inferecning using OpenVINO toolkit
The following components are required-

- OpenVINO toolkit
- Model Optimizer - For Openvino toolkit version < 2022.1 , Model optimizer is included in the toolkit. Whereas from 20221. versions onwards, Model optimizer need to be installed seperately.
- System – CPU/ GPU/ VPU
- Python
- ONNX
- Pytorch
- Netron model visualizer
