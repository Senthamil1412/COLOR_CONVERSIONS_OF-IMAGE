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

## Integrated by: Senthamil Selvan G
## Register No.: 212222230139


### i)Read and Display an Image
```
import matplotlib.pyplot as plt
import cv2
img=cv2.imread('lion.png')
plt.imshow(img)
plt.show()
```
![image](https://github.com/user-attachments/assets/478da8c0-635b-40fd-9e95-f8c7af4dcd4f)


### ii)Draw Shapes and Add Text
1) Draw a line from the top-left to the bottom-right of the image.
```
res=cv2.line(img,(0,0),(600,400),(205,100,250),10)
plt.imshow(res)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/87e15173-7bc3-47e4-aeab-b318c7af720e)



2) Draw a circle at the center of the image.
```
imc=cv2.imread('lion.png')
resc=cv2.circle(imc,(600,1000),125,(223,95,280),15)
plt.imshow(resc)
plt.axis('on')
plt.show()
```
![image](https://github.com/user-attachments/assets/2cffdf8e-820a-42a6-8bb0-4fc0f273f3ae)



3.Draw a rectangle around a specific region of interest in the image.
```
imr=cv2.imread('lion.png')
start=(250,250)
stop=(900,900)
color=(250,250,200)
thick=15
resr=cv2.rectangle(imr,start,stop,color,thick)
plt.imshow(resr)
plt.show()
```
![image](https://github.com/user-attachments/assets/b95f9895-3aa9-4f99-bdb3-007650073885)



4. Add the text "OpenCV Drawing" at the top-left corner of the image.
```
imt = cv2.imread("lion.png")
text = "OpenCV Drawing"
position = (100, 500)
font = cv2.FONT_HERSHEY_COMPLEX_SMALL
font_scale = 4
color = (252, 55, 255) 
thickness = 4
rest = cv2.putText(imt, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
plt.imshow(rest)
plt.show()

```
![image](https://github.com/user-attachments/assets/032982c1-8ee1-4a12-afe3-824db0934cc0)




### iii)Image Color Conversion
1. Convert the image from RGB to HSV and display it
```
image=cv2.imread("lion.png")
imhsv=cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
plt.imshow(imhsv)
plt.show()
```
![image](https://github.com/user-attachments/assets/dec5ca6a-10dd-4efe-81b4-2a8fe13a5546)


2. Convert the image from RGB to GRAY and display it.

```
image1=cv2.imread("lion.png",0)
imgs=cv2.cvtColor(image1, 0)
plt.imshow(imgs)
plt.show()
```
![image](https://github.com/user-attachments/assets/3ffaa5c2-27dc-4e00-875f-26a825623b01)



3. Convert the image from RGB to YCrCb and display it.
```
imrgb=cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
plt.imshow(imrgb)
plt.show()
```
![image](https://github.com/user-attachments/assets/c629e15d-26eb-436c-98a7-dd8cb7a9d48f)


### iv)Access and Manipulate Image Pixels
1. Access and print the value of the pixel at coordinates (100, 100)
```
im2=cv2.imread('lion.png')
p=im2[100,100]
p
```
array([8, 8, 8], dtype=uint8)


2. Modify the color of the pixel at (200, 200) to white.
```
imaw=cv2.imread("lion.png")
for i in range(100,250):
    for j in range(100,250):
        imaw[i,j]=225
plt.imshow(imaw,cmap="gray")
plt.show()
```
![image](https://github.com/user-attachments/assets/cf159c34-e111-4791-82cd-4765935cce88)



### v)Image Resizing
Resize the original image to half its size and display it.
```
ime=cv2.imread('lion.png')
ime.shape
```
(1800, 1200, 3)
```
image_resize=cv2.resize(ime,(150,150))
image_resize.shape
```
(150, 150, 3)


### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
imcr=cv2.imread("lion.png")
r1=imcr[0:250,0:250]
cv2.imwrite('CR1.jpg',r1)
imgc1=cv2.imread("CR1.jpg")
plt.imshow(imgc1)
plt.show()
```
![image](https://github.com/user-attachments/assets/4eaf2858-fa9c-48d0-af82-21aaf89b16f3)




### vii)Image Flipping
1. Flip the original image horizontally and display it.
```
imageho = cv2.imread("lion.png")
resho=cv2.rotate(imageho,cv2.ROTATE_180)
plt.imshow(resho)
plt.show()
```
![image](https://github.com/user-attachments/assets/ec659052-0572-4575-b540-065eba6ced89)



2. Flip the original image vertically and display it.
```
imageve = cv2.imread("lion.png")
resve=cv2.rotate(imageve,cv2.ROTATE_90_CLOCKWISE)
plt.imshow(resve)
plt.show()
```
![image](https://github.com/user-attachments/assets/900d21bb-4a29-4e43-85bd-2db01d626a0a)



### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```
cv2.imwrite('Saved.jpg',resve)
```
![image](https://github.com/user-attachments/assets/11ba08ea-1e42-4312-bd70-3ab32130e989)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.
