# Implementation-of-filter

### NAME : PRAVESH N
### REG NO : 212223230154

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
```py
# NAME : PRAVESH N
# REG NO : 212223230154
```

### 1. Smoothing Filters

## i) Using Averaging Filter
```py
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("Imgage2.jpg")
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
## ii) Using Weighted Averaging Filter
```py
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
## iii) Using Gaussian Filter
```py
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
## iv)Using Median Filter
```py
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
## i) Using Laplacian Linear Kernal
```py
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
## ii) Using Laplacian Operator
```py
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


## i) Using Averaging Filter

<img width="717" height="206" alt="Screenshot 2025-09-29 101821" src="https://github.com/user-attachments/assets/dd7c4ac6-aae9-4b35-bb31-34ee3ada3cd4" />


## ii)Using Weighted Averaging Filter

<img width="566" height="170" alt="Screenshot 2025-09-29 101900" src="https://github.com/user-attachments/assets/a16ba0af-1411-47ed-a2f5-29e7739c1e31" />


## iii)Using Gaussian Filter

<img width="526" height="170" alt="Screenshot 2025-09-29 101923" src="https://github.com/user-attachments/assets/6a07e52e-0697-442c-acfb-f97b35b353ea" />


## iv) Using Median Filter

<img width="724" height="223" alt="Screenshot 2025-09-29 101948" src="https://github.com/user-attachments/assets/9daf1b60-cf3b-4b29-87c6-6a7496e023d7" />


### 2. Sharpening Filters


## i) Using Laplacian Kernal

<img width="534" height="174" alt="Screenshot 2025-09-29 102010" src="https://github.com/user-attachments/assets/bdb37ff7-cfed-418b-aac8-278f0f310051" />


## ii) Using Laplacian Operator

<img width="533" height="166" alt="Screenshot 2025-09-29 102031" src="https://github.com/user-attachments/assets/3a05b91d-7ce7-4552-a900-04f487d6054f" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
