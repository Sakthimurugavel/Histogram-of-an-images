# EX 03 : Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()
### Step2:
Print the image using imshow().
### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.
### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.
### Step5:
The Histogram of gray scale image and color image is shown.

## Program:
```python
# Developed By: sakthivel.M
# Register Number: 212222230156

## Gray Image and Color Image
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("Ajith.jpeg")
color_image = cv2.imread("vijay.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

## Histogram of Grayscale Image
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('Ajith.jpeg')
color_img = cv2.imread('vijay.jpeg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(gray_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

## Histogram of Color Image
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('Ajith.jpeg')
color_img = cv2.imread('Vijay.jpeg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(color_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

## Histogram Equilization of GrayScale Image
import cv2
gray_img = cv2.imread('Ajith.jpeg',0)
gray_img = cv2.resize(gray_img,(300,200))
cv2.imshow('Grey Scale Image',gray_img)
equ = cv2.equalizeHist(gray_img)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)

```
## Output:
### Input Grayscale Image and Color Image
![out 1 ex 3](https://github.com/Sakthimurugavel/Histogram-of-an-images/assets/118707246/1b732278-3d09-4ec9-a89b-23ff443cf277)![out2 ex 3](https://github.com/Sakthimurugavel/Histogram-of-an-images/assets/118707246/afbeb56b-b15a-48a7-8ad0-2029699fcfe7)



### Histogram of Grayscale Image and any channel of Color Image
![out 3 1](https://github.com/Sakthimurugavel/Histogram-of-an-images/assets/118707246/a261aeba-4c2a-4f38-b899-0dd4d5378f46)![out 4 ex 3](https://github.com/Sakthimurugavel/Histogram-of-an-images/assets/118707246/94448355-72d1-4e77-be75-43e5ed310f5e)

### Histogram of Color Image:
![out 5,1 ex 3](https://github.com/Sakthimurugavel/Histogram-of-an-images/assets/118707246/b278f471-66ca-485b-bdce-aaaf2b5b34c5)![out 5,2 ex 3](https://github.com/Sakthimurugavel/Histogram-of-an-images/assets/118707246/bc3812b7-a680-40f8-b119-c49ef159aaa6)


### Histogram Equalization of Grayscale Image.
![out 6 e ex 3](https://github.com/Sakthimurugavel/Histogram-of-an-images/assets/118707246/17f9a51e-23dc-408d-b3c9-33c483d53234)![out 6 g ex 3](https://github.com/Sakthimurugavel/Histogram-of-an-images/assets/118707246/69d9c8c0-d197-4afd-89c1-bab09f19cfed)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
