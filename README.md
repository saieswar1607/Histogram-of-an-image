# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the necessary libraries and read two images, Color image and Gray Scale image.
<br>

### Step2:

Calculate the Histogram of Gray scale image and each channel of the color image.
<br>

### Step3:

Display the histograms with their respective images.
<br>

### Step4:

Equalize the grayscale image.
<br>

### Step5:

Display the grayscale image.
<br>

## Program:
```python
# Developed By:
# Register Number:
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.

gray_image=cv2.imread('grayscaleimage.jpg')
hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
plt.imshow(gray_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

# Display the histogram of gray scale image and any one channel histogram from color image

color_image=cv2.imread('car.jpg')
hist=cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.imshow(color_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('colorscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

# Write the code to perform histogram equalization of the image. 

gray_image = cv2.imread('gray.jpg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
<br>
<img width="463" alt="exp4_1_1" src="https://user-images.githubusercontent.com/93427011/166973065-bd522ec6-0007-416b-b4dd-74c6b8d053c0.png">
<br>

### Histogram of Grayscale Image and any channel of Color Image
<br>
<img width="463" alt="exp4_1_2" src="https://user-images.githubusercontent.com/93427011/166973672-21b8f4b7-3f50-4180-9329-f0b7a320c887.png">
<br>

### Histogram Equalization of Grayscale Image
<br>
<img width="200" alt="exp4_2_1" src="https://user-images.githubusercontent.com/93427011/166973407-b4db6360-f1db-404f-9a69-4bcfb2d1b7d3.png">
<br>
<img width="200" alt="exp4_2_2" src="https://user-images.githubusercontent.com/93427011/166973978-b5fd1de6-48aa-4369-9f6b-6d89c38add6e.png">
<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
