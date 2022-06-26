## EX NO:03
## DATE:11.4.22
# <p align="center">Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save and image as filename.jpg

### Step2:
Use imread(filename, flags) to read the file.

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:
Split and merge the image using cv2.split and cv2.merge commands

### Step5:
End the program and close the output image windows.

## Program:
```python
# Developed By: PRASHETHAA R
# Register Number:212220230036
  
# i) Convert BGR and RGB to HSV and GRAY
import cv2
color_image = cv2.imread('nature.jpg')
cv2.imshow('Original image',color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()




# ii)Convert HSV to RGB and BGR
import cv2
color_image = cv2.imread('nature.jpg')
cv2.imshow('Original image', color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()




# iii)Convert RGB and BGR to YCrCb
import cv2
color_image = cv2.imread('nature.jpg')
cv2.imshow('Original image',color_image)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()



# iv)Split and Merge RGB Image
import cv2
image = cv2.imread('nature.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
Merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',Merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()



# v) Split and merge HSV Image
import cv2
image = cv2.imread('nature.jpg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue-Image',h)
cv2.imshow('Saturation-Image',s)
cv2.imshow('Gray-Image',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()



```
## Output:
### i) BGR and RGB to HSV and GRAY
![Screenshot (219)](https://user-images.githubusercontent.com/75234942/162749671-dd91e492-55f7-4b67-a12b-4750cb433709.png)

### ii) HSV to RGB and BGR

![Screenshot (220)](https://user-images.githubusercontent.com/75234942/162749794-31ad0538-d3d7-46c3-b4fc-dc4dadc9cd79.png)

### iii) RGB and BGR to YCrCb
![Screenshot (221)](https://user-images.githubusercontent.com/75234942/162688999-26253e89-c1b6-45c4-aa09-f2aef121b203.png)


### iv) Split and merge RGB Image
![Screenshot (222)](https://user-images.githubusercontent.com/75234942/162749927-37bdeac9-ba82-4261-baad-b8fc04e7e237.png)
![Screenshot (223)](https://user-images.githubusercontent.com/75234942/162749994-39e3bd94-785e-49ab-8d3f-4a9dfd518ecc.png)

### v) Split and merge HSV Image
![Screenshot (224)](https://user-images.githubusercontent.com/75234942/162689129-a70d3e34-15b8-440c-a4c2-9cf9ac679f5b.png)
![Screenshot (225)](https://user-images.githubusercontent.com/75234942/162689538-1f95b1a5-56e1-4f57-a114-8a9435875068.png)




## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
