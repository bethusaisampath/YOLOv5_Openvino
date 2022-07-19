# Object Detection & YOLOs
Object detection is a technique of training computers to detect objects from images or videos. Over the years, there are many object detection architectures and algorithms created by multiple companies and researchers.

YOLO refers to “You Only Look Once” is one of the most versatile and famous object detection models. For every real-time object detection work, YOLO is the first choice by Data Scientist and Machine learning engineers. YOLO algorithms divide all the given input images into the SxS grid system. Each grid is responsible for object detection. Now those Grid cells predict the boundary boxes for the detected object. For every box, we have five main attributes: x and y for coordinates, w and h for width and height of the object, and a confidence score for the probability that the box containing the object.

The YOLO network consists of three main pieces-
1) Backbone - A convolutional neural network that aggregates and forms image features at different granularities.
2) Neck - A series of layers to mix and combine image features to pass them forward to prediction.
3) Head - Consumes features from the neck and takes box and class prediction steps.

## YOLOv5
After a few days of the release of the YOLOv4 model on 27 May 2020, YOLOv5 got released by [Glenn Jocher](https://www.linkedin.com/in/glenn-jocher/)(Founder & CEO of Utralytics). It was publicly released on Github [here](https://github.com/ultralytics/yolov5). Glenn introduced the YOLOv5 Pytorch based approach, and Yes! YOLOv5 is written in the Pytorch framework. With the continuous effort and 58 open source contributors, YOLOv5 set the benchmark for object detection models very high, it already beats the [EfficientDet](https://arxiv.org/pdf/1911.09070.pdf) and its other previous YOLO versions.

The largest contribution of YOLOv5 is to translate the Darknet research framework to the PyTorch framework. The Darknet framework is written primarily in C and offers fine grained control over the operations encoded into the network. In many ways the control of the lower level language is a boon to research, but it can make it slower to port in new research insights, as one writes custom gradient calculations with each new addition. Pytotch inferences are very fast that before releasing YOLOv5, many other AI practitioners often translate the YOLOv3 and YOLOv4 weights into Ultralytics Pytorch weight. There is no official YOLOV5 paper released yet and also many controversies are happening about its name.

# YOLOv5 Inferencing using OpenVINO toolkit
Now we will see how YOLOv5 model inferencing can be done using Intel OpenVINO toolkit.

The following components are required-

- OpenVINO toolkit
- Model Optimizer - For Openvino toolkit (version < 2022.1) , Model optimizer comes included in the toolkit. But for 2022.1 versions onwards, OpenVINO development tools (like model optimizer) need to be installed seperately.
- System – CPU/ GPU/ VPU
- Python
- ONNX
- Pytorch
- Netron model visualizer

## OpenVINO toolkit Installation
### For OpenVINO version < 2022.1
1) [Install](https://www.intel.com/content/www/us/en/developer/tools/openvino-toolkit/download-previous-versions.html) OpenVINO toolkit 2021.4 or 2021.3 or any other older version of your choice. Download and install suitable toolkit depending on your operating system. Follow all the required install instructions.
2) Here Model optimizer comes included in the toolkit.

### For OpenVINO version >= 2022.1
1) [Install](https://www.intel.com/content/www/us/en/developer/tools/openvino-toolkit/download.html) OpenVINO toolkit 2022.1 or any other recent version of your choice. Download and install suitable toolkit depending on your operating system. Follow all the required install instructions. Here the OpenVINO development tools are not included in the toolkit, they need to be installed seperately.
2) From the 2022.1 release, the [OpenVINO Development Tools](https://docs.openvino.ai/2022.1/openvino_docs_install_guides_install_dev_tools.html#doxid-openvino-docs-install-guides-install-dev-tools) (like Model Optimizer, Benchmark Tool, Accuracy Checker & Post-Training Optimization Tool, etc) can only be installed via [PyPI](https://pypi.org/project/openvino-dev/). Download and install the Development Tools Package from PyPI where we use Model optimizer for our YOLOv5 optimization.


