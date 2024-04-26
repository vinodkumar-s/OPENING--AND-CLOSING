## OPENING--AND-CLOSING
### Aim
To implement Opening and Closing using Python and OpenCV.

### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:
Import the necessary packages
#### Step2:
Create the Text using cv2.putText
#### Step3:
Create the structuring element
#### Step4:
Use Opening operation
#### Step5:
Use Closing Operation

### Program:
```
Developed by: VINOD KUMAR S
Register Number:212222240116
```
#### Display the input Image
```
import cv2
import numpy as np

img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'VINOD KUMAR', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)
```
#### Create ths structured element
```
struct_ele = np.ones((9, 9), np.uint8)
```
#### Display the result of Opening
```
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, struct_ele)
cv2.imshow('Opening', opening)
cv2.waitKey(0)
```
#### Display the result of Closing
```
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, struct_ele)
cv2.imshow('Closing', closing)
cv2.waitKey(0)
```
### Output:

#### Display the input Image

![Screenshot 2024-04-26 205000](https://github.com/vinodkumar-s/OPENING--AND-CLOSING/assets/113497226/b51f00e9-eae1-4fe1-a2d2-5ceb273ea097)


#### Display the result of Opening

![Screenshot 2024-04-26 205015](https://github.com/vinodkumar-s/OPENING--AND-CLOSING/assets/113497226/7046b6e2-e8ff-4e38-bcb6-249fa905efa6)


#### Display the result of Closing
![Screenshot 2024-04-26 205022](https://github.com/vinodkumar-s/OPENING--AND-CLOSING/assets/113497226/846011c1-104e-4b35-ab0e-28b0d3d022ab)




### Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
