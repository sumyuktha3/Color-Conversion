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
# Developed By:S.Sumyuktha Rani
# Register Number:21220230050
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

![1a](https://user-images.githubusercontent.com/75235818/163594134-15f642bd-fde8-494d-908e-45f49725d747.jpeg)
![1b](https://user-images.githubusercontent.com/75235818/163594142-ca35b5f7-92c8-42a5-a1c4-9d9ae4a542ec.jpeg)
![1c](https://user-images.githubusercontent.com/75235818/163594151-bb657b62-9276-4f33-8bf6-7f641a37d93a.jpeg)

### ii) HSV to RGB and BGR

![2a](https://user-images.githubusercontent.com/75235818/163594165-c2b0c082-7726-4418-9713-4e49e8aa3259.jpeg)

### iii) RGB and BGR to YCrCb

![3a](https://user-images.githubusercontent.com/75235818/163594211-8efaebdc-4c75-48af-8f7f-a6c556096f3c.jpeg)

### iv) Split and merge RGB Image

![4a](https://user-images.githubusercontent.com/75235818/163594234-9b15bd52-b3e8-4214-9b98-b9f10e4f143c.jpeg)
![4b](https://user-images.githubusercontent.com/75235818/163594247-4eec690c-dee3-4b13-b4f3-551874fcf787.jpeg)

### v) Split and merge HSV Image

![5a](https://user-images.githubusercontent.com/75235818/163594264-271af39e-756d-4254-bd32-c35410952dcb.jpeg)
![5b](https://user-images.githubusercontent.com/75235818/163594269-0aa5239d-b5f1-4df4-94c7-a19775167427.jpeg)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
