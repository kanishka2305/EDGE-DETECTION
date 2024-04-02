# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
```py
Developed by: Kanishka V S
Register Number: 212222230061
```
### Convert image to grayscale and remove noise:
```py
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("parrot.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
### SOBEL X AXIS :
```py
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
### SOBEL Y AXIS :
```py
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
### SOBEL XY AXIS :
```py
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR:
```py
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR:
```py
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR

### SOBEL X AXIS:
![image](https://github.com/kanishka2305/EDGE-DETECTION/assets/113497357/c4252422-c65a-425c-8ab6-8931e705b56a)

### SOBEL Y AXIS :
![image](https://github.com/kanishka2305/EDGE-DETECTION/assets/113497357/c0c3b1a4-92dc-48e6-a6a6-62c6752ff7d3)

### SOBEL XY AXIS :
![image](https://github.com/kanishka2305/EDGE-DETECTION/assets/113497357/e0a00353-1244-4ab6-b683-b6d98b175f4d)

### LAPLACIAN EDGE DETECTOR
![image](https://github.com/kanishka2305/EDGE-DETECTION/assets/113497357/7f15d807-2531-4116-8c46-c5971e4c5e29)

### CANNY EDGE DETECTOR
![image](https://github.com/kanishka2305/EDGE-DETECTION/assets/113497357/31c32f1e-7e6d-40d5-bd58-efd09b665e0f)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
