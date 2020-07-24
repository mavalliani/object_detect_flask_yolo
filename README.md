# Object Detection with YOLO3
Yolov3 is an algorithm that uses deep convolutional neural networks to perform object detection. This repository implements Yolov3 using TensorFlow 2.0 and creates two easy-to-use APIs that you can integrate into web or mobile applications. <br>

## Quick Start

```bash
# Tensorflow CPU
1. conda env create -f conda-cpu.yml
2. conda activate yolov3-cpu
3. pip install -r requirements.txt
4. wget https://pjreddie.com/media/files/yolov3.weights -O weights/yolov3.weights
5. python load_weights.py
6. python app.py

Endpoints:
1. [POST] ./image
  a. key: images
  b. value: image
```
![example](https://github.com/theAIGuysCode/Object-Detection-API/blob/master/detections/detection.jpg)

```bash
2. [POST] ./detections
  a. key: images
  b. value: image
  
```

```
{
  "response": [
    {
      "detections": [
        {
          "class": "dog",
          "confidence": 99.77
        },
        {
          "class": "bicycle",
          "confidence": 99.01
        },
        {
          "class": "truck",
          "confidence": 93.9
        }
      ],
      "image": "dog.jpg"
    }
  ]
}
```
