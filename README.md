# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### Developed By: Sharangini T K
### Register Number: 212222230143


## Output:

### i)Read and Display an Image
```
import cv2
image=cv2.imread('shara.jpg',1)
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 160724](https://github.com/user-attachments/assets/e94de2b0-ad27-4fd7-b85c-0a5b765808d8)


<br>
<br>

### ii)Draw Shapes and Add Text
i)Draw a line from the top-left to the bottom-right of the image.
```
import cv2
img = cv2.imread("shara.jpg")
res = cv2.line(img, (0, 0), (338, 601), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 161403](https://github.com/user-attachments/assets/b85338d8-0fac-4f25-905f-4de29c0d803e)


ii)Draw a circle at the center of the image.
```
import cv2

# Load the image
img = cv2.imread("shara.jpg")

# Get the dimensions of the image
height, width, _ = img.shape

# Calculate the center of the image
center_coordinates = (width // 2, height // 2)

# Draw a circle at the center of the image
res = cv2.circle(img, center_coordinates, 80, (255, 0, 0), 10)

# Display the image with the circle
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 161745](https://github.com/user-attachments/assets/f80a0154-dab7-4633-9e33-4827d9f309e0)


iii)Draw a rectangle around a specific region of interest in the image.
```
import cv2

img = cv2.imread("shara.jpg")
start=(100,100)
stop=(300,400)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(img,start,stop,color,thickness)
# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 162450](https://github.com/user-attachments/assets/201688dd-bc61-420b-9bc0-7ff87644b902)


iv)Add the text "PANDA" at the top-left corner of the image.
```
import cv2

# Load the image
img = cv2.imread("shara.jpg")

# Define the text to be added and its position
text = "NATURE"
position = (50, 50)  # Positioning the text at the top-left corner

# Set the font, scale, color, and thickness of the text
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)  # White color
thickness = 2

# Add the text to the image
res = cv2.putText(img, text, position, font, font_scale, color, thickness, cv2.LINE_AA)

# Display the image with the text
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![Screenshot 2024-09-09 162619](https://github.com/user-attachments/assets/7be2f6fd-eec4-47cf-9637-7f8d237a409e)


<br>
<br>

### iii)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```
import cv2
img = cv2.imread('shara.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 162830](https://github.com/user-attachments/assets/e6b0085f-2a83-43bc-9987-d959bbfc46e5) ![Screenshot 2024-09-09 162817](https://github.com/user-attachments/assets/d4192b7b-fc52-450d-9553-6d77859013f7)



ii.)Convert the image from RGB to GRAY and display it.
```
import cv2
img = cv2.imread('shara.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 162916](https://github.com/user-attachments/assets/71f2a469-8751-4869-9bc6-c5c8f6bc9bfc) ![Screenshot 2024-09-09 162930](https://github.com/user-attachments/assets/d19ac83f-3cd5-4a01-a340-e6b8973fd4e1)

 
iii.)Convert the image from RGB to YCrCb and display it.
```
import cv2
img = cv2.imread('shara.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 163001](https://github.com/user-attachments/assets/10a03444-d73f-4f06-97fa-e374cf7138ba) ![Screenshot 2024-09-09 163015](https://github.com/user-attachments/assets/46d9f58b-02d7-447b-acb4-87baabcbdfcb)


iv.)Convert the HSV image back to RGB and display it.
```
import cv2
img = cv2.imread('shara.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 163054](https://github.com/user-attachments/assets/e86839a3-4497-407f-9a90-d73af3dac4a4) ![Screenshot 2024-09-09 163105](https://github.com/user-attachments/assets/172eb647-dd5a-41e6-9adc-fe3e7de42014)



<br>
<br>

### iv)Access and Manipulate Image Pixels
```
import cv2

# Load and resize the image
img = cv2.imread('shara.jpg', 1)
img = cv2.resize(img, (300, 200))

# Show the original image
cv2.imshow('Original Image', img)

# 1. Access and print the value of the pixel at coordinates (100, 100)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")

# 2. Modify the color of the pixel at (199, 199) to white
img[199, 199] = [255, 255, 255]  # Setting the pixel value to white (BGR)

# Display the modified image
cv2.imshow('Modified Image', img)

# Wait for a key press and close the windows
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 233207](https://github.com/user-attachments/assets/9fdf2377-fa54-4c1a-97ab-d31a3fbf1857)


![Screenshot 2024-09-09 222125](https://github.com/user-attachments/assets/843aeff6-8197-4139-929c-9b9b9ca01c10) ![Screenshot 2024-09-09 222140](https://github.com/user-attachments/assets/71818644-70bd-4d72-883b-338aa2294bc1)


<br>
<br>

### v)Image Resizing
```
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(image, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 222223](https://github.com/user-attachments/assets/69862ccb-4a0f-4b3f-b71c-718e45e4976f) ![Screenshot 2024-09-09 222238](https://github.com/user-attachments/assets/2d5eddc3-234d-4cb3-bc3b-49eacc60d4fe)


<br>
<br>

### vi)Image Cropping
```
import cv2

# Load the image
image1=cv2.imread('shara.jpg',1)

# Define the starting point and size of the ROI
x, y = 50, 50
width, height = 100, 100

# Crop the ROI
roi = image1[y:y + height, x:x + width]

# Display the cropped ROI
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 233542](https://github.com/user-attachments/assets/105efff7-4017-4adf-881f-90e261b78187)

<br>
<br>

### vii)Image Flipping
i.)Flip the original image horizontally and display it.
```
import cv2
img = cv2.imread("shara.jpg")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 222601](https://github.com/user-attachments/assets/f53a65b1-27e4-4bfb-88d0-cea35c4a9520) ![Screenshot 2024-09-09 222623](https://github.com/user-attachments/assets/ad74eb58-c1cb-4b16-b4b8-b09cdcd0a85c)


ii.)Flip the original image vertically and display it.
```
import cv2

img = cv2.imread("shara.jpg")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-09-09 222712](https://github.com/user-attachments/assets/7c883612-ef6c-4847-90f4-f20bccc74c76) ![Screenshot 2024-09-09 222724](https://github.com/user-attachments/assets/4347d597-f05c-4d9a-8615-3ac13f448c64)

<br>
<br>

### viii)Write and Save the Modified Image
```
 cv2.imwrite('nature.jpg',image)
```
![Screenshot 2024-09-09 234133](https://github.com/user-attachments/assets/3b602cfe-145d-4e6b-84bc-8e6c6e45b5a4)

<br>
<br>






## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.

