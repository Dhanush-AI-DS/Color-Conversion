# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1: Import cv2 and save and image as filename.jpg
<br>

### Step2: Use imread(filename, flags) to read the file.
<br>

### Step3: Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.
<br>

### Step4: Split and merge the image using cv2.split and cv2.merge commands.
<br>

### Step5: End the program and close the output image windows.
<br>

## Program:
```python
# Developed By: DHANUSH S
# Register Number: 212221230020 

# i) Convert BGR and RGB to HSV and GRAY

import cv2
house_color_image = cv2.imread('bear.jpg')
cv2.imshow('Original image',house_color_image)
hsv_image = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_image)
hsv_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_image1)
gray_image = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_image)
gray_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_image1)

cv2.waitKey(0)
cv2.destroyAllWindows()


# ii)Convert HSV to RGB and BGR

import cv2
sun_color_image = cv2.imread('bear.jpg')
cv2.imshow('Original image', sun_color_image)
hsv_image = cv2.cvtColor(sun_color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()



# iii)Convert RGB and BGR to YCrCb

import cv2
sun_color_image = cv2.imread('bear.jpg')
cv2.imshow('Original image', sun_color_image)
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()


# iv)Split and Merge RGB Image


import cv2
image = cv2.imread('bear.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()

# v) Split and merge HSV Image

import cv2
image = cv2.imread('bear.jpg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('H',h)
cv2.imshow('S',s)
cv2.imshow('V',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()


```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>![Out](bee-01.png)
<br>

### ii) HSV to RGB and BGR
<br>![Out](bee-02.png)
<br>

### iii) RGB and BGR to YCrCb
<br>![Out](bee-03.png)
<br>

### iv) Split and merge RGB Image
<br>![Out](bee-04.png)
<br>

### v) Split and merge HSV Image
<br>![Out](bee-05.png)
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
