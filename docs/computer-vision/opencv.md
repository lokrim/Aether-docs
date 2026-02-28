---
id: opencv
title: OpenCV Guide
sidebar_position: 2
---

# OpenCV

[OpenCV](https://opencv.org/) (Open Source Computer Vision Library) is an open-source computer vision and machine learning software library. It contains hundreds of optimized algorithms for image and video analysis.

## Installation

Once you have your Python virtual environment activated, you can install OpenCV using `pip`:

```bash
pip install opencv-python
```

If you also need the contrib modules (which include extra algorithms):
```bash
pip install opencv-contrib-python
```

## Basic Usage

Here is a quick example of how to read an image and display it using OpenCV:

```python
import cv2

# Read an image from file
image = cv2.imread('example.jpg')

# Check if image was successfully loaded
if image is not None:
    # Convert image to grayscale
    gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

    # Display the image in a window
    cv2.imshow('Grayscale Image', gray_image)

    # Wait indefinitely until a key is pressed
    cv2.waitKey(0)

    # Destroy all open windows
    cv2.destroyAllWindows()
else:
    print("Error: Could not load the image.")
```

> **Note:** OpenCV reads images in **BGR** (Blue, Green, Red) format by default, not standard RGB!

## Key Concepts to Study

1. **Image processing:** Grayscaling, blurring, thresholding, edge detection.
2. **Video capture:** Reading from a webcam (`cv2.VideoCapture`).
3. **Drawing:** Drawing rectangles, lines, and text on frames (useful for bounding boxes).

## Resources
- [OpenCV-Python Tutorials (Official)](https://docs.opencv.org/4.x/d6/d00/tutorial_py_root.html)
- [PyImageSearch](https://pyimagesearch.com/) - Excellent hands-on tutorials.
