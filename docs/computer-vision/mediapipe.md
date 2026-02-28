---
id: mediapipe
title: MediaPipe Guide
sidebar_position: 3
---

# MediaPipe

[MediaPipe](https://mediapipe.dev/) is a framework by Google for building cross-platform, customizable ML solutions for live and streaming media. It is exceptionally good at very fast edge-inference for tasks like hand tracking, face detection, and pose estimation.

## Why use MediaPipe?

- **Real-time Performance:** Models run blazingly fast even on CPU.
- **Pre-trained Models:** No need to collect data and train models from scratch for common CV tasks like hands and body poses.
- **Cross-platform:** Works on Android, iOS, web, desktop, and more.

## Installation

Ensure your virtual environment is active, then install:

```bash
pip install mediapipe
```

## Basic Usage (Hand Tracking Example)

Here is a simple example showing how to initialize the MediaPipe Hands solution on a webcam feed:

```python
import cv2
import mediapipe as mp

# Initialize MediaPipe Hands
mp_hands = mp.solutions.hands
hands = mp_hands.Hands(
    static_image_mode=False,
    max_num_hands=2,
    min_detection_confidence=0.5
)
mp_drawing = mp.solutions.drawing_utils

# Open webcam
cap = cv2.VideoCapture(0)

while cap.isOpened():
    ret, frame = cap.cap.read()
    if not ret:
        break

    # Convert BGR to RGB (MediaPipe requires RGB)
    rgb_frame = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    
    # Process the frame to find hands
    results = hands.process(rgb_frame)

    # Draw hand landmarks if detected
    if results.multi_hand_landmarks:
        for hand_landmarks in results.multi_hand_landmarks:
            mp_drawing.draw_landmarks(
                frame, 
                hand_landmarks, 
                mp_hands.HAND_CONNECTIONS
            )

    cv2.imshow('MediaPipe Hands', frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cap.release()
cv2.destroyAllWindows()
```

## Resources

- [MediaPipe Solutions Overview](https://developers.google.com/mediapipe/solutions)
- [MediaPipe Hand Tracking Guide](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker)
