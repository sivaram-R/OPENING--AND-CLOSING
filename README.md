# EX 10 OPENING AND CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Give the input text using cv2.putText()
- Step3: Perform opening operation and display the result
- Step4: Similarly, perform closing operation and display the result
## Program:
NAME: Sivaram R
REG.No:212222100050 
# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
cv2.putText(img1,'CYBERSECURITY',(5,70), font,2,(255),5,cv2.LINE_AA)
```
# Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
```python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```
# Use Closing Operation
```python
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:
### Display the input Image
![image](https://github.com/sivaram-R/OPENING--AND-CLOSING/assets/121165794/2e59d48c-6fdf-4943-9a1c-53e1f419f469)
### Display the result of Opening
![image](https://github.com/sivaram-R/OPENING--AND-CLOSING/assets/121165794/f8d0ff15-f462-4667-8564-1985d55db58f)
### Display the result of Closing
![image](https://github.com/sivaram-R/OPENING--AND-CLOSING/assets/121165794/86f53c0f-d023-4333-9f88-5c15ae9c37ec)
## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
