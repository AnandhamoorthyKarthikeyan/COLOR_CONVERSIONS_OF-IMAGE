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
	Draw a line from the top-left to the bottom-right of the image.
	Draw a circle at the center of the image.
	Draw a rectangle around a specific region of interest in the image.
	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
	Convert the image from RGB to HSV and display it.
	Convert the image from RGB to GRAY and display it.
	Convert the image from RGB to YCrCb and display it.
	Convert the HSV image back to RGB and display it.

### Step4:
	Access and print the value of the pixel at coordinates (100, 100).
	Modify the color of the pixel at (200, 200) to white.

### Step5:
	Resize the original image to half its size and display it.
### Step6:
	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
	Flip the original image horizontally and display it.
	Flip the original image vertically and display it.
### Step8:
	Save the final modified image to your local directory.
```
Developed By: ANANDHAMOORTHY.K
Register Number: 212222100004
```
# Program:

### 1)Read and Display an Image

```Python
import cv2
image=cv2.imread('loki.jpg')
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
``` 
 

### OUTPUT:
![Screenshot 2024-09-11 155935](https://github.com/user-attachments/assets/41bb929b-1493-4531-9f60-14f19c6a10a7)
### 2.) Draw Shapes and Add Text:
i)Draw a line from the top-left to the bottom-right of the image.

```Python
import cv2
img = cv2.imread('loki.jpg')
img=cv2.resize(img,(600,800))
res = cv2.line(img, (0, 0), (599, 799), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
<br>
<br>


### OUTPUT:
![Screenshot 2024-09-10 112851](https://github.com/user-attachments/assets/9b99afea-b8f3-4c2c-95f5-eccd340b4630)

### ii)Draw Shapes and Add Text
```Python
import cv2


img = cv2.imread('loki.jpg')
img1=cv2.resize(img,(600,800))


height, width, _ = img1.shape


center_coordinates = (width // 2, height // 2)


res = cv2.circle(img1, center_coordinates, 150, (255, 0, 0), 10)

cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
<br>
<br>


### OUTPUT:
![Screenshot 2024-09-10 114719](https://github.com/user-attachments/assets/4f8860ab-2044-4b9e-965d-5378aa089014)
  
### iii)Draw a rectangle around a specific region of interest in the image.
```Python

import cv2
img = cv2.imread('loki.jpg')
img1=cv2.resize(img,(600,800))
start=(0,0)
stop=(409,529)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(img1,start,stop,color,thickness)

cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
 <br>
 <br>

### OUTPUT:
![Screenshot 2024-09-10 114736](https://github.com/user-attachments/assets/81205664-f568-4b7b-b850-9e35180cb360)

 
### iv)Add the text "OpenCV Drawing" at the top-left corner of the image.

 ```Python
import cv2

img = cv2.imread('loki.jpg')
img1=cv2.resize(img,(600,800))

text = "OPENCV DRAWING"
position = (50, 50)  # Positioning the text at the top-left corner

font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)  # White color
thickness = 2


res = cv2.putText(img1, text, position, font, font_scale, color, thickness, cv2.LINE_AA)


cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
<br>
<br>

    
### OUTPUT:

![Screenshot 2024-09-10 114746](https://github.com/user-attachments/assets/e5648615-d962-4009-abac-a8eead002fd2)

### 3)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```Python
import cv2
img = cv2.imread('loki.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### OUTPUT:
![Screenshot 2024-09-10 115429](https://github.com/user-attachments/assets/11677c8a-230e-4d92-8450-1e9cdc83574f)

#### ii.)Convert the image from RGB to GRAY and display it.
```Python
import cv2
img = cv2.imread('loki.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output:
![Screenshot 2024-09-10 115457](https://github.com/user-attachments/assets/e0ce4173-b727-4391-b3ec-adcf14bc8d36)


#### iii.)Convert the image from RGB to YCrCb and display it.
```Python
import cv2
img = cv2.imread('loki.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Output:
![Screenshot 2024-09-10 115513](https://github.com/user-attachments/assets/b7181fff-db8b-43da-8c07-70c502f0a20d)

#### iv.)Convert the HSV image back to RGB and display it.
```Python
import cv2
img = cv2.imread('loki.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output:
![Screenshot 2024-09-10 115525](https://github.com/user-attachments/assets/f2b96b6c-d53a-4b81-b733-cbb955b62704)

## 4. Access and Manipulate Image Pixels:
```Python
import cv2
img = cv2.imread('loki.jpg')
img = cv2.resize(img, (300, 200))
cv2.imshow('Original Image', img)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
img[199, 199] = [255, 255, 255]
cv2.imshow('Modified Image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:
![Screenshot 2024-09-10 115543](https://github.com/user-attachments/assets/f6d9a0f3-776c-4a2a-bcb7-661a01af6bef)

## 5. Image Resizing:
```Python
import cv2
img = cv2.imread('loki.jpg')
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(img, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:
![Screenshot 2024-09-10 115559](https://github.com/user-attachments/assets/86ac976b-5fa6-4516-b579-bfe1ecf2d057)

## 6.Image Cropping:
```Python
import cv2
img = cv2.imread('loki.jpg')
img1=cv2.resize(image1,(600,800))
x, y = 50, 50
width, height = 100, 100
roi = image1[y:y + height, x:x + width]
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output:
![Screenshot 2024-09-10 115628](https://github.com/user-attachments/assets/d5142047-8a21-453b-8e22-47d68656aa9c)

## 7.Image Flipping:
i.)Flip the original image horizontally and display it.
```Python
import cv2
img = cv2.imread('loki.jpg')
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output:
![Screenshot 2024-09-11 150845](https://github.com/user-attachments/assets/fa770b8d-ea78-4c39-b9c4-d0d15e68ed59)

#### ii.)Flip the original image vertically and display it.

```Python
import cv2
img = cv2.imread('loki.jpg')
img1=cv2.resize(img,(600,800))
img = cv2.resize(img1,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:
![Screenshot 2024-09-11 150917](https://github.com/user-attachments/assets/7fb57d99-411a-42da-a7b8-081e70a37423)

## 8. Write and Save the Modified Image:
```Python
import cv2
img = cv2.imread('loki.jpg')
img = cv2.resize(img,(300,200))
cv2.imwrite('lokesh1.jpg',img)
```
<br>
<br>

### Output:
![Screenshot 2024-09-10 115054](https://github.com/user-attachments/assets/edc8170d-4543-4a79-879f-f1a8b06a29b1)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.
