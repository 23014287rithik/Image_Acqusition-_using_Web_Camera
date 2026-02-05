# Image_Acqusition-_using_Web_Camera
## Name: RITHIK V
## Register no:212223230171

## Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Import OpenCV Package.

### Step 2:
Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.

### Step 3:
Read Video or Image. Utilize 'imread' to read a video frame or image from the webcam.

### Step 4:
Save Image to File. Employ 'imwrite' to save the captured image to a file.

### Step 5:
Display Video or Image. Use 'imshow' to display the captured video frame or image.

### Step 6:
End Program with 'q'. Allow the program to be terminated by pressing the 'q' key.


## Program:
### Developed By: RITHIK V
### Register No: 212223230171

## i) Write the frame as JPG file

```PYTHON
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


## ii) Display the video

```PYTHON
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


## iii) Display the video by resizing the window

```PYTHON

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
  

```


## iv) Rotate and display the video

```PYTHON
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

### i) Write the frame as JPG image
</br>

<img width="512" height="409" alt="2b6a2e15-88f4-482c-873d-79542e84f677" src="https://github.com/user-attachments/assets/301b79ef-0957-441d-bdbe-87bb2e449c94" />

</br>


### ii) Display the video
</br>
<img width="512" height="389" alt="7fce667f-4066-422b-a40b-56c5d694e096" src="https://github.com/user-attachments/assets/d22dd4e3-0b2d-4037-b397-970308c99bbd" />

</br>


### iii) Display the video by resizing the window
</br>
<img width="266" height="389" alt="2823e351-53fb-4d6a-99a3-c097acc27cf9" src="https://github.com/user-attachments/assets/60a8f7dc-b0d7-4451-8d11-3c932abf5049" />

</br>



### iv) Rotate and display the video
</br>
<img width="297" height="389" alt="77462185-686d-4cd8-915a-7854d4ba3f0c" src="https://github.com/user-attachments/assets/fb91af33-5f62-4fee-809a-689fd7c0c3a0" />

</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
