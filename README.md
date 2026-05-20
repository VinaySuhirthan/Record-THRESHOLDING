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

<img width="435" height="291" alt="image" src="https://github.com/user-attachments/assets/ee3305fd-85a9-48d8-8580-5f9d8bbafbdc" />

<br>

### Global Thresholding
<br>

<img width="434" height="288" alt="image" src="https://github.com/user-attachments/assets/f21a0986-db61-41e4-9a73-27ca97af3b31" />

<br>

### Adaptive Thresholding
<br>
<img width="426" height="293" alt="image" src="https://github.com/user-attachments/assets/d05bed6e-f85b-4e76-9ba8-b4500766c982" />


<br>

### Optimum Global Thesholding using Otsu's Method
<br>

<img width="473" height="290" alt="image" src="https://github.com/user-attachments/assets/5f8e407a-4b68-49fa-8937-0add9aa8d300" />

<br>


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
