# Ex-3-Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```
# Developed By: SANTHANA LAKSHMI K
# Register Number: 212222240091
``` 
```python


import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('gray_image.jpeg')
color_image = cv2.imread('color_image.jpg')
cv2.imshow("Gray image",gray_image)
cv2.imshow("color image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

import numpy as np
gray_image=cv2.imread('gray_image.jpeg')
import matplotlib.pyplot as plt 
gray_hist=cv2.calcHist(gray_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()

import numpy as np
color_image=cv2.imread('color_image.jpg')
import matplotlib.pyplot as plt 
color_hist=cv2.calcHist(color_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(color_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()

import cv2
gray_image = cv2.imread("gray_image.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:
### Input Grayscale Image and Color Image
![color_image](https://github.com/user-attachments/assets/d7449ce5-2a5c-446b-a295-e16755b9314b)

![2024-09-25 (5)](https://github.com/user-attachments/assets/8cbc5b2d-dcf4-45cf-93f8-0bb7b4d05c22)

### Histogram of Grayscale Image and any channel of Color Image

#### Grayscale Image

![2024-09-25 (8)](https://github.com/user-attachments/assets/b24bde4a-489f-4984-a584-50cef8c406d4)

#### Color Image

![2024-09-25 (9)](https://github.com/user-attachments/assets/06c48f8f-a637-4d17-9103-017e17ada977)

### Histogram Equalization of Grayscale Image.

![2024-09-25 (4)](https://github.com/user-attachments/assets/ecf052ad-4a2f-4964-a8b2-0a46b488bc9e)

![2024-09-25 (5)](https://github.com/user-attachments/assets/140eca5a-3bc4-4200-a791-f2c848142451)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
