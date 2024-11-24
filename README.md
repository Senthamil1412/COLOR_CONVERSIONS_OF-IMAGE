# COLOR_CONVERSIONS_OF-IMAGE

## AIM


#### To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv) To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:

### Anaconda - Python 3.7

## Algorithm:


### Step 1

Choose an image and save it as a filename.jpg 

### Step 2

Use imread(filename, flags) to read the file.


### Step 3

Use imshow(window_name, image) to display the image.

### Step 4

Use imwrite(filename, image) to write the image.

### Step 5

End the program and close the output image windows.


### Step 6

Convert BGR and RGB to HSV and GRAY

### Step 7

Convert HSV to RGB and BGR

### Step 8

Convert RGB and BGR to YCrCb

### Step 9

Split and Merge RGB Image


### Step 10

Split and merge HSV Image

Developed By: PRAVEEN S

Register Number: 212222240078


#### IMAGE 

![ex1](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/f32ed665-7965-4326-90c6-6c76594a7e41)


## Program:


### (i) Read and display the image
```py
#Read and display the image
import cv2
image=cv2.imread('ex1.jpg',1)
image=cv2.resize(image,(200,325))
cv2.imshow('Psv',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Output:

![image](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/a4c33ef9-beeb-46cf-aa3c-09d5a6d35fe9)


## Program:

### (ii) Write the image

```py
#Write the image
import cv2
image=cv2.imread('ex1.jpg',0)
cv2.imwrite('demos.jpg',image)
```

### Output

![image](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/3ada3b26-8930-43cc-80e9-1f9c81ce7dcc)


## Program:

### (iii) Shape of the Image

```py
#Shape of the Image
import cv2
image=cv2.imread('ex1.jpg',1)
print(image.shape)
```


### Output 

![image](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/fe1aeed9-6e4b-4590-8060-876c41a4553f)


## Program:

### (iv) Access rows and columns
```py
#Access rows and columns
import random
import cv2
image=cv2.imread('ex1.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                    random.randint(0,255),
                    random.randint(0,255)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Output

![image](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/ef0fca26-5867-4791-b975-f26aa7b41670)



## Program:

### (v) Cut and paste portion of image
```py
#Cut and paste portion of image
import cv2
image=cv2.imread('ex1.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('partimage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output
![image](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/b53fecbd-b3ba-456a-8375-f1d44b869ca8)


## Program:

### (vi) BGR and RGB to HSV and GRAY
```py
#BGR and RGB to HSV and GRAY
import cv2
img = cv2.imread('ex1.jpg',1)
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
### Original Image

![image](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/92303789-e323-4eb9-ba0e-0fdce69427cd)


### Output

![image](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/01ea9fcd-66c7-44fb-ab2f-5c4eada4afa0)


## Program:

### (vii) HSV to RGB and BGR

```py
#HSV to RGB and BGR
import cv2
img = cv2.imread('ex1.jpg')
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

### Original HSV

![image](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/5692de82-493b-400c-b4b1-e5b9c9f47909)


### Output

![image](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/6b48c6b2-6ecf-4e5a-9b07-257e165e9fe0)



## Program:

### (viii) RGB and BGR to YCrCb
```py

#RGB and BGR to YCrCb
import cv2
img = cv2.imread('ex1.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output

![image](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/311b94e8-aa32-4c80-95ee-52a177832a0d)

## Program:

### (ix) Split and merge RGB Image
```py
#Split and merge RGB Image
import cv2
img = cv2.imread('ex1.jpg',1)
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
### Output

#### Channels

![image](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/1b50bf45-b1c0-4fdc-89ca-ceb06d664775)


#### Merged RGB

![image](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/cdfa696d-7ceb-48ed-a61b-100f4f3a1740)

## Program:

### (x) Split and merge HSV Image
```py
#Split and merge HSV Image
import cv2
img = cv2.imread("ex1.jpg",1)
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

### Output

### Merged HSV


![image](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/a7399fa6-f2ed-44d6-83c2-fbe0392e915d)


### Splitted


![image](https://github.com/Praveen0500/COLOR_CONVERSIONS_OF-IMAGE/assets/120218611/aad81f9b-8954-41fd-95f9-2a8caa479eb5)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
