# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step1: Import the necessary libraries and read two images, Color image and Gray Scale image

Step2: Calculate the Histogram of Gray scale image and each channel of the color image.

Step3: Display the histograms with their respective images.

Step4: Equalize the grayscale image.

Step5: Display the grayscale image.

## Program:
```python
# Developed By:Marella Dharanesh
# Register Number:212222240062

# Write your code to find the histogram of gray scale image and color image channels.

import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread('gt.jpeg')
color_image = cv2.imread('gt 650.jpeg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(color_image)
plt.show()


# Display the histogram of gray scale image and any one channel histogram from color image


import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("gt.jpeg")
color_image = cv2.imread("gt 650.jpeg")
gray_hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()


# Write the code to perform histogram equalization of the image. 

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('gt.jpeg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![WhatsApp Image 2023-04-04 at 20 13 48](https://user-images.githubusercontent.com/118707669/229855531-a1cdad37-e17f-47cd-b66f-e16317c0c42c.jpg)

### Histogram of Grayscale Image and any channel of Color Image

![WhatsApp Image 2023-04-04 at 20 14 03](https://user-images.githubusercontent.com/118707669/229855451-8dd185a2-b6ce-4a36-af71-f34928737545.jpg)

### Histogram Equalization of Grayscale Image
![WhatsApp Image 2023-04-04 at 20 14 14](https://user-images.githubusercontent.com/118707669/229855231-a5050453-919a-44b1-925a-64531d3ea88b.jpg)

## Result:
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
