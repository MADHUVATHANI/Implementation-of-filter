# Implementation-of-filter

## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.
### Step2
Convert the image from BGR to RGB.
### Step3
Apply the required filters for the image separately.
### Step4
Plot the original and filtered image by using matplotlib.pyplot.
### Step5
End the program.
## Program:
### Developed By   : MADHUVATHANI V
### Register Number:212223040107
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("a.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters

i) Using Averaging Filter
<img width="768" height="300" alt="image" src="https://github.com/user-attachments/assets/8d9f29a3-969b-4141-b9a6-685dc8557e8b" />


ii)Using Weighted Averaging Filter
<img width="546" height="238" alt="image" src="https://github.com/user-attachments/assets/6b9f4fe2-b9b3-4fc1-a74e-a358177b06df" />


iii)Using Gaussian Filter
<img width="541" height="232" alt="image" src="https://github.com/user-attachments/assets/9d5f7ff8-8a50-4da0-8e2d-a0f1bf29a8db" />

iv) Using Median Filter
<img width="727" height="293" alt="image" src="https://github.com/user-attachments/assets/2bb77fd6-238e-4f2b-87e6-a4640f92d8cf" />

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
<img width="583" height="229" alt="image" src="https://github.com/user-attachments/assets/eb8ca8d1-2f94-4989-b2db-430775cd4c80" />


ii) Using Laplacian Operator
<img width="527" height="234" alt="image" src="https://github.com/user-attachments/assets/eb96dec0-aa45-4e4b-9c3b-c7e2b3ed5b26" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
