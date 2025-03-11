# License Plate Detection and Recognition using YOLOv8

## Overview

This project utilizes YOLOv8 for license plate detection and YOLOv8-OBB (Oriented Bounding Box) for character recognition. The system detects license plates from images or videos, recognizes characters, and overlays the detected text back onto the media.

## Pipeline

### Data Preprocessing

Before training and inference, the input data is preprocessed to improve model accuracy and robustness:

Format Conversion: Convert annotations and images into YOLO format.

Data Augmentation:

Rotation: Randomly rotate images to simulate different viewing angles.

Noise Addition: Introduce Gaussian noise to improve model generalization.

Brightness & Contrast Adjustment: Vary image brightness and contrast to handle diverse lighting conditions.

Motion Blur: Apply motion blur to simulate moving vehicles.

Perspective Transformations: Adjust perspective to simulate different camera angles.

### License Plate Detection

YOLOv8 is used to detect license plates in images or video frames. The detected plates are cropped and passed to the next stage for character recognition.

### Character Recognition

YOLOv8-OBB is applied to extract and recognize individual characters within the detected license plates. The model is trained to handle different fonts, orientations, and distortions.

### Result Overlay

The recognized license plate number is displayed directly on the processed image or video for visualization and verification.


