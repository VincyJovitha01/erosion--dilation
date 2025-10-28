# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

## Program:

### Import the necessary packages
``` 
import cv2
import numpy as np
from matplotlib import pyplot as plt
```


### Load the image
```
img1=np.zeros((100,700),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
```
### Create the text using cv2.putText
```

cv2.putText(img1,'JEFFY BRILIN' ,(5,70),font,4,(255),2,cv2.LINE_AA)

``` 

### Create the structuring element

```
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

```

### Erode the image

```
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)
```


### Dilate the image
```

plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')


```
## Output:

### Display the input Image

<img width="501" height="507" alt="image" src="https://github.com/user-attachments/assets/4d8fe004-2909-4539-bb5f-065d465a7fe9" />

### Display the Eroded Image

<img width="553" height="517" alt="image" src="https://github.com/user-attachments/assets/74addc45-813e-4323-9b7e-99bb1a37f9e5" />

### Display the Dilated Image

<img width="500" height="527" alt="image" src="https://github.com/user-attachments/assets/70b8595e-ef03-47c4-8f02-446aaa4853fd" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
