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
### Developed By:Senthamil Selvan G
### Register Number: 212222230139


## Output:

### i)Read and Display an Image
```
import cv2
image=cv2.imread('b.jpg',1)
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/d5aed9b0-7c19-4ef1-84a8-6ee19c031df5)

<br>
<br>

### ii)Draw Shapes and Add Text
i)Draw a line from the top-left to the bottom-right of the image.
```
import cv2
img = cv2.imread("b.jpg")
res = cv2.line(img, (0, 0), (1099, 799), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
![image](https://github.com/user-attachments/assets/32667b3d-d6f8-4f64-91d4-f1edc24b6064)

ii)Draw a circle at the center of the image.
```


import cv2

img = cv2.imread("b.png")

res=cv2.circle(img,(100,100),100,(200,0,0),10)

# Display the HSV image
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/4fa7cabe-c7ba-4d6b-b1fe-327e2708ade6)

iii)Draw a rectangle around a specific region of interest in the image.
```
import cv2

img = cv2.imread("panda.jpg")
start=(0,0)
stop=(318,200)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(img,start,stop,color,thickness)
# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/e33ec6d8-29fb-4713-a567-3fc60f2e9431)


iv)Add the text "PANDA" at the top-left corner of the image.
```
import cv2

# Load the image
img = cv2.imread("panda.JPG")

# Define the text to be added and its position
text = "OPENCV DRAWING"
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

![image](https://github.com/user-attachments/assets/7bfdcd9e-a9ea-41bf-bc30-bf7d77d132a0)

<br>
<br>

### iii)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```
import cv2
img = cv2.imread('panda.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/ebe21ed0-727e-431e-a614-caa4dcd32246)

ii.)Convert the image from RGB to GRAY and display it.
```
import cv2
img = cv2.imread('panda.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/84199410-5b2e-44e8-8099-62ba4d279a14)
iii.)Convert the image from RGB to YCrCb and display it.
```
import cv2
img = cv2.imread('panda.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/15046968-99eb-4028-a524-5c2d01042766)
iv.)Convert the HSV image back to RGB and display it.
```
import cv2
img = cv2.imread('panda.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![image](https://github.com/user-attachments/assets/1f50d6d5-f749-40ab-a7da-685e0ab655bb)

<br>
<br>

### iv)Access and Manipulate Image Pixels
```
import cv2

# Load and resize the image
img = cv2.imread('panda.jpg', 1)
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
![image](https://github.com/user-attachments/assets/5e2f0fe3-ecfa-4d45-8f93-7da690b373df)


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

![image](https://github.com/user-attachments/assets/68aa3cda-136c-4cce-a2cd-a8313c71a963)
![image](https://github.com/user-attachments/assets/588aa82f-4371-43cd-9e90-2b821cd1f4fc)

<br>
<br>

### vi)Image Cropping
```
import cv2

# Load the image
image1=cv2.imread('panda.jpg',1)

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

<br>
<br>

### vii)Image Flipping
i.)Flip the original image horizontally and display it.
```
import cv2
img = cv2.imread("panda.jpg")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/6d75f529-ddad-4827-8c2e-c2de775079d2)
ii.)Flip the original image vertically and display it.
```
import cv2

img = cv2.imread("panda.JPG")
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/a73e4e00-3ea0-47fb-9cf3-90af75caab05)


<br>
<br>

### viii)Write and Save the Modified Image
```
 cv2.imwrite('panda.jpg',image)
```
![image](https://github.com/user-attachments/assets/a2ab057a-430d-492a-be5b-988cc0ccde5d)

<br>
<br>






## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







