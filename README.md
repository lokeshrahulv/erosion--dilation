# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

## Program:

``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'MADHAV',(40,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
# Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
```
# Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
# Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![image](https://github.com/lokeshrahulv/erosion--dilation/assets/118423842/16315647-c4c2-452e-b288-d30db38d0c58)

### Display the Eroded Image
![Screenshot 2024-05-01 153955](https://github.com/lokeshrahulv/erosion--dilation/assets/118423842/3f4def65-be51-4f6c-916a-278e31145386)

### Display the Dilated Image
![Screenshot 2024-05-01 154026](https://github.com/lokeshrahulv/erosion--dilation/assets/118423842/dcdfb2d9-58f4-4c34-b32c-e425583a5db5)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
