# Image-Acquisition-from-Web-Cameraa
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
<br>

### Step 2:
<br>

### Step 3:
<br>

### Step 4:
<br>

### Step 5:
<br>

## Program:
``` Python
### Developed By:
### Register No:

## i) Write the frame as JPG file




## ii) Display the video




## iii) Display the video by resizing the window





## iv) Rotate and display the video









```
## Output

### i) Write the frame as JPG image
```
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("NewPicture.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```
### ii) Display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('IYYANAR S (212222240036)',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```

### iii) Display the video by resizing the window
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('IYYANAR S (212222240036)',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```

### iv) Rotate and display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('IYYANAR S (212222240036)',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
### i) Write the frame as JPG image
![DIP 21](https://github.com/Iyyanar22009120/Image-Acquisition-from-Web-Cameraa/assets/118680259/05486d75-1f72-4274-9772-ab4e71a481ca)
### ii) Display the video
![DIP22](https://github.com/Iyyanar22009120/Image-Acquisition-from-Web-Cameraa/assets/118680259/13b0dcbe-b423-4b92-b31c-6bbc1ab52ec8)
### iii) Display the video by resizing the window
![DIP23](https://github.com/Iyyanar22009120/Image-Acquisition-from-Web-Cameraa/assets/118680259/ba0413ed-c36c-4d68-ad31-ff80009d5f8e)
### iv) Rotate and display the video
![DIP24](https://github.com/Iyyanar22009120/Image-Acquisition-from-Web-Cameraa/assets/118680259/21986b43-f64c-4a6e-9941-9519c4ac7dba)


## Result:
Thus the image is accessed from webcamera and displayed using openCV.
