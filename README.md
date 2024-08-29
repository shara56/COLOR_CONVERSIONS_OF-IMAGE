# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By: Sharangini T K
### Register Number: 212222230143


## Output:

### i) Read and display the image

```
import cv2
image=cv2.imread('boat.jpg',1)
image = cv2.resize(image, (400, 300))
cv2.imshow('BOAT',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![1](https://github.com/user-attachments/assets/9e4db735-6649-49b4-a7fc-467d8e5f7693)

### ii)Write the image

```
cv2.imwrite('b.jpg',image)
```
![2](https://github.com/user-attachments/assets/9a6b269d-235c-44c1-aeea-bf7e1f67b08b)

### iii)Shape of the Image

```
print(image.shape)
```
![3](https://github.com/user-attachments/assets/de88cf4b-a055-4080-a45d-59b181e71867)

### iv)Access rows and columns

```
import random
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                     random.randint(0,255),
                     random.randint(0,255)] 
cv2.imshow('boat1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![4](https://github.com/user-attachments/assets/26d79c83-2512-4d9f-af28-e85155b3bd37)

### v)Cut and paste portion of image
```
image=cv2.imread('boat.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[130:200,110:190]
image[110:180,120:200] = tag
cv2.imshow('boat2',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![5](https://github.com/user-attachments/assets/d5d3e3b0-8739-4170-bbdc-dcfddfb29812)

### vi) BGR and RGB to HSV and GRAY
```
img = cv2.imread('boat.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![6](https://github.com/user-attachments/assets/9f47d279-004d-41b0-91b5-72d472d57fa3)

### vii) HSV to RGB and BGR
```
img = cv2.imread('boat.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![7](https://github.com/user-attachments/assets/eb550f11-1589-4d9e-8954-2d05ef4a5129)

### viii) RGB and BGR to YCrCb
```
img = cv2.imread('boat.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![8](https://github.com/user-attachments/assets/11fe6819-8091-4bfe-81fa-bf8b37d6af60)

### ix) Split and merge RGB Image
```
img = cv2.imread('boat.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![9](https://github.com/user-attachments/assets/4f1c4f95-8854-431e-adab-ed4b2fd0effb)

### x) Split and merge HSV Image
```
img = cv2.imread("boat.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![10](https://github.com/user-attachments/assets/65f26c23-370d-4826-bffb-cef20cab300b)




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.



