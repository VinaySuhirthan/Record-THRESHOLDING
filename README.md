# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages.

### Step2:
Read the Image and convert to grayscale.

### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.

## Program

## NAME : K S Vinay Suhirthan
## REG NO : 212224230305

## Load the necessary packages
```py
import cv2
import matplotlib.pyplot as plt

```

## Read the Image and convert to grayscale
```py
image=cv2.imread('pic.jpeg')
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```
## Original Image
```py
plt.subplot(2,2,1)
plt.imshow(cv2.cvtColor(image,cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
## Use Global thresholding to segment the image
```py
_,global_thresholded = cv2.threshold(gray_img, 127, 255, cv2.THRESH_BINARY)
```

## Use Adaptive thresholding to segment the image
```py
adaptive_thresholded = cv2.adaptiveThreshold(gray_img, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
```

## Use Otsu's method to segment the image
```py
_,otsu_thresholded = cv2.threshold(gray_img, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
```
## Global Thresholding
```py
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```

## Adaptive Thresholding
```py
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
## Otsu's Method
```py
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
## Show the plot
```py
plt.tight_layout()
plt.show()
```


## Output

### Original Image
<br>
<img width="500" height="400" alt="image" src="https://github.com/user-attachments/assets/06a44eb9-a7c7-4233-978e-8510cee1a3a2" />

<br>

### Global Thresholding
<br>
<img width="500" height="400" alt="image" src="https://github.com/user-attachments/assets/8490c5e1-5b28-43c5-a0df-9e28d3148b16" />

<br>

### Adaptive Thresholding
<br>
<img width="500" height="400" alt="image" src="https://github.com/user-attachments/assets/c0ee3ea2-4555-4d66-a5ce-2d85be7ac6e1" />

<br>

### Optimum Global Thesholding using Otsu's Method
<br>
<img width="500" height="400" alt="image" src="https://github.com/user-attachments/assets/7edf71d8-1009-428a-8ef3-1c7b91aba390" />

<br>


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
