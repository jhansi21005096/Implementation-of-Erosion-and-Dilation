# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import the necessary packages.

### Step2:

Create the Text using cv2.putText.
### Step3:

Create the structuring element.
### Step4:

Erode the image.
### Step5:

Dilate the image.
 
## Program:

``` Python
# Import the necessary packages

import cv2
import matplotlib.pyplot as plt
import numpy as np

# Create the Text using cv2.putText
img1=np.zeros((90,250),dtype='uint8')
img2=cv2.cvtColor(img1,cv2.COLOR_BGR2RGB)
font=cv2.FONT_HERSHEY_DUPLEX
cv2.putText(img2,'JHANSI',(5,70),font,2,(51, 193, 245),3,cv2.LINE_8)
plt.imshow(img2)

# Create the structuring element

kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7

# Erode the image

image_erode1=cv2.erode(img2,kernel1)
plt.imshow(image_erode1)

# Dilate the image

image_dilate=cv2.dilate(img2,kernel1)
plt.imshow(image_dilate)

```
## Output:

### Display the input Image
![output](https://github.com/jhansi21005096/Implementation-of-Erosion-and-Dilation/blob/main/Screenshot%202023-05-10%20at%201.19.02%20PM.png)

### Display the Eroded Image
![output](https://github.com/jhansi21005096/Implementation-of-Erosion-and-Dilation/blob/main/Screenshot%202023-05-10%20at%201.19.14%20PM.png)

### Display the Dilated Image
![output]()
## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
