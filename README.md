# Histogram-of-an-images
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
```python
# Developed By: SANTHANA LEKSHMI K 
# Register Number: 212222240091

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('grey image.jpg')
color_image = cv2.imread('color image.jpeg')
cv2.imshow("Gray image",gray_image)
cv2.imshow("color image",color_image)

import numpy as np
gray_image=cv2.imread('grey image.jpg')
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
color_image=cv2.imread('color image.jpeg')
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
gray_image = cv2.imread("grey image.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image

![2024-09-25](https://github.com/user-attachments/assets/d2391592-8384-4296-b55e-7268d65b3dbf)



![2024-09-25 (1)](https://github.com/user-attachments/assets/2529b564-bc54-4ee8-97c3-72851c106ddd)

### Histogram of Grayscale Image and any channel of Color Image
![2024-09-25 (2)](https://github.com/user-attachments/assets/895f24b6-348d-4dc9-87b1-5ae4a34ca725)

![2024-09-25 (3)](https://github.com/user-attachments/assets/b57dad4f-e62e-4f9a-8c21-7f0c3b88a0cf)


### Histogram Equalization of Grayscale Image.

### Gray Image



![image](https://github.com/user-attachments/assets/9d223fe3-7dbb-40f7-89bf-7fbb34763248)

### Equalixation Image



![image](https://github.com/user-attachments/assets/1fa12fbc-ee14-4209-8192-3e3642f47287)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
