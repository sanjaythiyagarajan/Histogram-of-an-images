# Histogram of images
## Aim
### To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
### Anaconda - Python 3.7

## Algorithm:
### Step1:
#### Read the gray and color image using imread()

### Step2:
#### Print the image using imshow().

### Step3:
#### Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
#### Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
#### The Histogram of gray scale image and color image is shown.


## Program:

### Colour and Gray Image

py
# Developed By: SANJAY T
# Register Number: 212222110039

```import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("dhoni1.jpeg")
color_image = cv2.imread("dhoni2.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Histogram of Grayscale Image

```py
import numpy as np
import cv2
Gray_image = cv2.imread("dhoni1.jpeg")
Color_image = cv2.imread("dhoni2.jpeg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```

### Histogram of Green channel of colour Image

```py
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)

```


```py

import cv2
gray_image = cv2.imread("dhoni2.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## Output:

### Input Grayscale Image and Color Image

![Screenshot 2024-03-11 204848](https://github.com/sanjaythiyagarajan/Histogram-of-an-images/assets/119409242/063cd9e5-75fa-43a7-a4da-0bd2ffeb0155)



### Histogram of Grayscale Image

![Screenshot 2024-03-11 205152](https://github.com/sanjaythiyagarajan/Histogram-of-an-images/assets/119409242/75b2bb7d-b640-47bb-84b3-b45e2a5b37c0)

### Histogram of Green Channel of colour Image

![Screenshot 2024-03-11 205350](https://github.com/sanjaythiyagarajan/Histogram-of-an-images/assets/119409242/3b0ea67e-403f-47c7-ad49-ae2493ec8f31)


### Histogram Equalization of Grayscale Image.

![Screenshot 2024-03-11 205720](https://github.com/sanjaythiyagarajan/Histogram-of-an-images/assets/119409242/c52eb1b0-edcd-481f-a352-fb5a4892581b)



## Result: 
### Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
