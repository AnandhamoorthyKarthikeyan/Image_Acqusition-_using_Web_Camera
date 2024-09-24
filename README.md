# Image_Acqusition-_using_Web_Camera
## Aim
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera
<br>

### Step 2:
Use cv2.imread to read the video or image
<br>

### Step 3:
Use cv2.imwrite to save the image
<br>

### Step 4:
Use cv2.imshow to show the video
<br>

### Step 5:
End the program and close the output video window by pressing 'q'.
<br>

## Program:
``` Python
Developed By: ANANDHAMOORTHY.K
Register No: 212222100004
```

## i) Write the frame as JPG file
```Python
import cv2
cap = cv2.VideoCapture (0)
frame_number = 0
while frame_number < 5:
    ret, frame = cap.read()
    cv2.imshow('frame', frame)
    cv2.imwrite(f"frame_{frame_number}.jpg", frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## ii) Display the video
```Python
import cv2
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    cv2.imshow('Video', frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iii) Display the video by resizing the window
```Python
import cv2
cap = cv2.VideoCapture (0) 
cv2.namedWindow('Video', cv2.WINDOW_NORMAL)
while True:
    ret, frame = cap.read()
    cv2.imshow('Video', frame)
    cv2.resizeWindow('Video', 100, 200)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iv) Rotate and display the video
```Python
import cv2
cap = cv2.VideoCapture (0)
while True:
    ret, frame = cap.read()
    rotated_frame=cv2.rotate(frame,cv2.ROTATE_90_CLOCKWISE)
    cv2.imshow('Rotated Video', rotated_frame)
    cv2.imwrite(f"frame_{frame_number}.jpg", frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output
### i) Write the frame as JPG image
![Screenshot 2024-09-24 113943](https://github.com/user-attachments/assets/85d2458f-2eee-43e5-808a-1b93f7f6b568)

</br>
</br>

### ii) Display the video
![Screenshot 2024-09-24 113943](https://github.com/user-attachments/assets/f7fec8a0-b42b-4bcd-b4e2-3e8de729c567)


</br>
</br>

### iii) Display the video by resizing the window


</br>
</br>

### iv) Rotate and display the video
![Screenshot 2024-09-24 114521](https://github.com/user-attachments/assets/bad361a8-6e53-4f4c-a510-3829adf61ba4)

</br>
</br>

## Result:
Thus the image is accessed from webcamera and displayed using openCV.
