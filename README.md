# Exp-9--Record-IMPLEMENTATION-OF-EROSION-AND-DILATION
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
import the neccesary packages
### Step2:
create the text using cv2.put Text
### Step3:
create the structuting element
### Step4:
Erodde the image
### Step5:
Dilate the image

 
## Program:

``` 
import cv2
import numpy as np
from matplotlib import pyplot as plt
imput_image='actor.jpg'
color_image=cv2.imread(imput_image)
gray_image=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)
edges=cv2.Canny(gray_image,100,200)
kernel_size=5
kernel=np.ones((kernel_size,kernel_size),np.uint8)
erosion=cv2.erode(edges,kernel,iterations=1)
dilation=cv2.dilate(edges,kernel,iterations=1)
plt.figure(figsize=(15,10))
plt.subplot(2,3,1)
plt.imshow(cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')
plt.subplot(2,3,2)
plt.imshow(gray_image,cmap='gray')
plt.title('black and white image')
plt.axis('on')
plt.subplot(2,3,3)
plt.imshow(edges,cmap='gray')
plt.title('edge segmentation')
plt.axis('on')
plt.subplot(2,3,4)
plt.imshow(edges,cmap='gray')
plt.title('erosion')
plt.axis('on')
plt.subplot(2,3,5)
plt.imshow(edges,cmap='gray')
plt.title('dilation')
plt.axis('on')

```
## Output:

### Display the input Image
<img width="469" height="466" alt="image" src="https://github.com/user-attachments/assets/9368b57a-cbd8-4776-8fc5-e59034235954" />

### Display the Eroded Image
<img width="457" height="461" alt="image" src="https://github.com/user-attachments/assets/cd13ce2e-2c0d-4f91-94b7-9d814b17cb00" />

### Display the Dilated Image

<img width="461" height="456" alt="image" src="https://github.com/user-attachments/assets/9b3974b6-7a9c-4341-a2ed-56c58731fde9" />

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
