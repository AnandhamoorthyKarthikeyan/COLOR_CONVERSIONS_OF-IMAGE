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
Developed By: THRIKESHWAR P
Register Number: 212222230162
```
# Program:

### 1)Read and Display an Image

```Python
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('lk.webp', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(img_rgb, cmap='viridis')   for RGB images
plt.title("Original Image")
plt.axis('off')  
plt.show()
``` 
 

### OUTPUT:
![image](https://github.com/user-attachments/assets/f0678048-1e29-4113-b286-933ac12423e2)




### 2.) Draw Shapes and Add Text:
i)Draw a line from the top-left to the bottom-right of the image.

```Python
image = cv2.imread('lk.webp') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
line_img = cv2.line(img_rgb, (0, 0), (1200, 900), (255, 0, 0), 2)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```
<br>
<br>


### OUTPUT:
![image](https://github.com/user-attachments/assets/f9de134c-1682-4ca5-9d74-faa4a97ddf28)


 
### ii)Draw Shapes and Add Text
```Python
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
circle_img = cv2.circle(img_rgb,(600,450),150,(255,0,0),10)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```
<br>
<br>


### OUTPUT:
![image](https://github.com/user-attachments/assets/1b2f7b01-a25c-474e-95c7-d7ba005fd52f)

### iii)Draw a rectangle around a specific region of interest in the image.
```Python
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (1200, 900), (0, 0, 255), 10)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```
 <br>
 <br>

### OUTPUT:
![image](https://github.com/user-attachments/assets/7b680000-ce70-48d4-a1c6-2ae8c99275b4)

### iv)Add the text "OpenCV Drawing" at the top-left corner of the image.

 ```Python
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```
<br>
<br>

    
### OUTPUT:
![image](https://github.com/user-attachments/assets/eb9066c2-cc76-4584-b510-2271fa798da0)





### 3)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```Python
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
```


### OUTPUT:
![image](https://github.com/user-attachments/assets/e6228b7e-4cd9-4b9a-acf1-34aecefd2f7f)



#### ii.)Convert the image from RGB to GRAY and display it.
```Python
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
```

### Output:
![image](https://github.com/user-attachments/assets/f3deb616-fba1-4e40-bd3b-f2715899a951)




#### iii.)Convert the image from RGB to YCrCb and display it.
```Python
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")

```
### Output:
![image](https://github.com/user-attachments/assets/4de1acbd-c009-4d1e-a157-1c053b3c937e)



#### iv.)Convert the HSV image back to RGB and display it.
```Python
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/cd43ce68-4ce4-4c7b-980c-cc5637b83f60)




## 4. Access and Manipulate Image Pixels:
```Python
image[200:500, 200:500] = [255, 255, 255]
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/73a10b4f-e6f7-4f7f-bb2f-d8f4f677ed6a)



## 5. Image Resizing:
```Python
resized_image = cv2.resize(image, (1200 // 2, 900 // 2))
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/218240c3-194f-4635-90d5-7dc51a76592c)



## 6.Image Cropping:
```Python
roi = image[50:350, 50:350]
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/600a4d56-8c02-43b2-8c75-504eb06a11e7)





## 7.Image Flipping:
i.)Flip the original image horizontally and display it.
```Python
flipped_horizontally = cv2.flip(image, 1)
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/68c12d2b-0e49-4044-9f8d-470ea1132d3a)






#### ii.)Flip the original image vertically and display it.

```Python
flipped_vertically = cv2.flip(image, 0)
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/176b0bb3-4fe9-46a4-a10f-15c28948f833)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







