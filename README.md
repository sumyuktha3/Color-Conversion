# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
```
Read an image using imread() and Convert BGR and RGB to HSV and GRAY
using:
cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```
### Step2:
```
Convert HSV to RGB and BGR
using:
cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
```
### Step3:
```
Convert RGB and BGR to YCrCb
using:
cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
```
### Step4:
```
Split and Merge RGB Image
using:
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.merge((blue,green,red))
```

### Step5:
```
Split and merge HSV Image
using:
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.merge((h,s,v))
```
## Program:
# Developed By: S.Sumyuktha Rani
# Register Number:212220230050

# i) Convert BGR and RGB to HSV and GRAY
```
import cv2
image=cv2.imread("pic.jpeg")
cv2.imshow("212220230040",image)
BGR_HSV=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR to HSV image",BGR_HSV)
BGR_GRAY=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR to GRAY image",BGR_GRAY)
RGB_HSV=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB to HSV image",RGB_HSV)
RGB_GRAY=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB to GRAY image",RGB_GRAY)
cv2.imshow("Apple",image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# ii)Convert HSV to RGB and BGR
```
sv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("HSV image",hsv)
HSV_RGB=cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV to RGB image",HSV_RGB)
HSV_BGR=cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV to BGR image",HSV_BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# iii)Convert RGB and BGR to YCrCb
```
RGB_YCrCb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB to YCrCb image",RGB_YCrCb)
BGR_YCrCb=cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR to YCrCb image",BGR_YCrCb)
cv2.imshow("picz",image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# iv)Split and Merge RGB Image
```
blue = image[:,:,0]
cv2.imshow("Blue Split",blue)
green = image[:,:,1]
cv2.imshow("Green Split",green)
red = image[:,:,2]
cv2.imshow("Red Split",red)
merged=cv2.merge((blue,green,red))
cv2.imshow("Merged Image",merged)
cv2.imshow("new pic",image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# v) Split and merge HSV Image
```
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.imshow('h_plane', h)
cv2.imshow('s_plane', s)
cv2.imshow('v_plane', v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow("HSV image",hsv)
cv2.imshow('Merged HSV',mergedhsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### i) BGR and RGB to HSV and GRAY

![1a](https://user-images.githubusercontent.com/75235818/163754855-72041407-cfe6-49d5-b09d-d4e693f29f07.jpeg)
![1b](https://user-images.githubusercontent.com/75235818/163754862-f5d0cc91-b874-4fe6-8d60-94706329133d.jpeg)
![1c](https://user-images.githubusercontent.com/75235818/163754868-26a0a16d-01cd-4823-90ea-f1e63df0229e.jpeg)

### ii) HSV to RGB and BGR

![2a](https://user-images.githubusercontent.com/75235818/163754888-631c157d-be07-457c-b27b-ee2087b92e91.jpeg)

### iii) RGB and BGR to YCrCb

![3a](https://user-images.githubusercontent.com/75235818/163754905-0dfb7a14-a73e-45a4-8f6b-cd01af646eb6.jpeg)

### iv) Split and merge RGB Image

![4a](https://user-images.githubusercontent.com/75235818/163754921-e3fdb751-55e9-4a01-b686-f82784a11682.jpeg)
![4b](https://user-images.githubusercontent.com/75235818/163754942-7a7c83a5-5e95-48ab-a4a4-a47d952cc013.jpeg)

### v) Split and merge HSV Image

![5a](https://user-images.githubusercontent.com/75235818/163754976-fc047246-4c46-47da-a68b-1fc47d237c23.jpeg)
![5b](https://user-images.githubusercontent.com/75235818/163754990-752b60c8-3512-46b1-8f98-031451a85c82.jpeg)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
