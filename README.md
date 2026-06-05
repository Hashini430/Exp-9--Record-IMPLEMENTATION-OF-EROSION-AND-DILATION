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
## Import Libraries

## PROGRAM
```python
import cv2
import numpy as np
from matplotlib import pyplot as plt
```

## Load Input Image

```python
input_image = 'actor.jpg'
color_image = cv2.imread(input_image)
```

## Convert Color Image to Grayscale

```python
gray_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2GRAY)
```

## Perform Edge Detection

```python
edges = cv2.Canny(gray_image, 100, 200)
```

## Create Kernel for Morphological Operations

```python
kernel_size = 5
kernel = np.ones((kernel_size, kernel_size), np.uint8)
```

## Apply Erosion

```python
erosion = cv2.erode(edges, kernel, iterations=1)
```

## Apply Dilation

```python
dilation = cv2.dilate(edges, kernel, iterations=1)
```

## Create Figure

```python
plt.figure(figsize=(15, 10))
```

## Display Original Color Image

```python
plt.subplot(2, 3, 1)
plt.imshow(cv2.cvtColor(color_image, cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')
```

## Display Grayscale Image

```python
plt.subplot(2, 3, 2)
plt.imshow(gray_image, cmap='gray')
plt.title('Black and White Image')
plt.axis('on')
```

## Display Edge Segmentation

```python
plt.subplot(2, 3, 3)
plt.imshow(edges, cmap='gray')
plt.title('Edge Segmentation')
plt.axis('on')
```

## Display Erosion Result

```python
plt.subplot(2, 3, 4)
plt.imshow(erosion, cmap='gray')
plt.title('Erosion')
plt.axis('on')
```

## Display Dilation Result

```python
plt.subplot(2, 3, 5)
plt.imshow(dilation, cmap='gray')
plt.title('Dilation')
plt.axis('on')
```

## Show Output

```python
plt.tight_layout()
plt.show()
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
