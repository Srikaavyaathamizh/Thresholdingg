# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
<br>
Translation moves the image along the x or y-axis.

### Step2:
<br>
Scaling resizes the image by scaling factors.

### Step3:
<br>
Shearing distorts the image along one axis.


### Step4:
<br>
Reflection flips the image horizontally or vertically.



### Step5:
<br>
Rotation rotates the image by a given angle.


## Program
NAME: SRIKAAVYAA T
REG NO: 212223230214

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('dhdd.jpg') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Original Image")
plt.axis('off')

_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')


plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')


plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

plt.tight_layout()
plt.show()

```
## Output

### Original Image
![image](https://github.com/user-attachments/assets/9cc6adc8-ad95-4405-a726-879f6cbca459)

### Global Thresholding
![image](https://github.com/user-attachments/assets/84060006-6f00-47ba-b810-9f8f30e040c1)

### Adaptive Thresholding
![image](https://github.com/user-attachments/assets/1a0a52da-84fe-4d3f-8ab6-3a28820b926c)

### Optimum Global Thesholding using Otsu's Method
![image](https://github.com/user-attachments/assets/ec366944-1188-4c96-b4f8-e843304cd5d4)


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
