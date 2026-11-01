# EXP-2-Record-Image-Acquisition-using-Web-Camera-212224230284

## NAME : SWETHA K
## REGISTER NUMBER : 212224230284
## EXPERIMENT : IMAGE ACQUISITION USING WEB CAMERA

## Aim

To develop a Python program using OpenCV to capture images and video frames from a webcam and perform basic image operations such as saving the captured frame as a JPG file, displaying the live video, resizing the frames, and rotating the video.

## Procedure
Step 1: Import the required libraries such as OpenCV, NumPy, Matplotlib, and other necessary modules.

Step 2: Initialize the webcam using cv2.VideoCapture(0) and read the video frames.

Step 3: Capture a frame from the webcam and save it as a JPG image using cv2.imwrite().

Step 4: Read and display the captured image using Matplotlib.

Step 5: Display the live webcam video by continuously capturing and showing frames.

Step 6: Resize the captured video frames using cv2.resize() and display the resized output.

Step 7: Rotate the video frames by 90 degrees clockwise using cv2.rotate() and display the rotated output.

Step 8: Release the webcam resources after completing all the operations.

## Program 

## Developed By: SWETHA K

## Register Number: 212224230284

## i) Write the Frame as a JPG File

```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time

cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()

captured_image = cv2.imread('captured_frame.jpg')

plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()

```

## ii) Display the Video

```

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()

```

## iii) Display the Video by Resizing the Frame

```

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()

```

## iv) Rotate and Display the Video

```

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()

```
## Output

## i) Write the Frame as a JPG Image

<img width="722" height="520" alt="image" src="https://github.com/user-attachments/assets/cb3143ea-1f83-494c-b7d5-425aeff87d9b" />

## ii) Display the Video

<img width="802" height="520" alt="image" src="https://github.com/user-attachments/assets/4b4b3dfd-989e-4ea6-b381-9ea1e3035544" />

## iii) Display the Video by Resizing the Frame

<img width="352" height="476" alt="image" src="https://github.com/user-attachments/assets/ee5acdce-b165-4313-93d1-8a278f26be8f" />

## iv) Rotate and Display the Video

<img width="387" height="497" alt="image" src="https://github.com/user-attachments/assets/128863ab-0d90-4c61-a2ba-f731948eb242" />

## Result: 

## Result

Thus, the webcam was successfully used to capture and save images in JPG format. The video was displayed, resized, and rotated using OpenCV, demonstrating basic image acquisition and manipulation techniques.

