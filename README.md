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

## Program:
### Developed By: Shaik Shoaib Nawaz
### Register Number: 212222240094
### i) Read and display the image:
```
import cv2
image = cv2.imread('Desktop/dipt/COLOR_CONVERSIONS_OF-IMAGE/shoaib.png', 1)
if image is None:
    print("Error: Image not found. Please check the file path.")
else:
    image = cv2.resize(image, (200, 300))
    cv2.imshow('Shaik Shoaib Nawaz', image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
### ii)Write the image:
```
    import cv2
    image=cv2.imread('Desktop/dipt/COLOR_CONVERSIONS_OF-IMAGE/shoaib.png',0)
    cv2.imwrite('shoaib.png',image)
```
### iii)Shape of the Image:
```
    import cv2
    image=cv2.imread('shoaib.png',1)
    print(image.shape)
```
### iv)Access rows and columns:
```
    import random
    import cv2
    image=cv2.imread('Desktop/dipt/COLOR_CONVERSIONS_OF-IMAGE/shoaib.png',1)
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
### v)Cut and paste portion of image:
```
 import cv2
   image=cv2.imread('Desktop/dipt/COLOR_CONVERSIONS_OF-IMAGE/shoaib.png',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('partimage1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
### vi) BGR and RGB to HSV and GRAY:
```
import cv2
img = cv2.imread('Desktop/dipt/COLOR_CONVERSIONS_OF-IMAGE/shoaib.png',1)
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
### vii) HSV to RGB and BGR:
```
import cv2
img = cv2.imread('Desktop/dipt/COLOR_CONVERSIONS_OF-IMAGE/shoaib.png')
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
### viii) RGB and BGR to YCrCb:
```
import cv2
img = cv2.imread('Desktop/dipt/COLOR_CONVERSIONS_OF-IMAGE/shoaib.png')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### ix) Split and merge RGB Image:
```
import cv2
img = cv2.imread('Desktop/dipt/COLOR_CONVERSIONS_OF-IMAGE/shoaib.png',1)
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
### x) Split and merge HSV Image:
```
import cv2
img = cv2.imread("Desktop/dipt/COLOR_CONVERSIONS_OF-IMAGE/shoaib.png",1)
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









## Output:

### i) Read and display the image:
![read img](image1.png)

<br>
<br>

### ii)Write the image:
![img_write](image2.png)
<br>
<br>

### iii)Shape of the Image:
![shape](image3.png)
<br>
<br>

### iv)Access rows and columns:
![accessing](image4.png)

<br>
<br>

### v)Cut and paste portion of image:
![alt text](image5.png)
<br>
<br>

### vi) BGR and RGB to HSV and GRAY:
![color](image6.png)
<br>
<br>

### vii) HSV to RGB and BGR:
![HSV](image7.png)
<br>
<br>

### viii) RGB and BGR to YCrCb:
![img_rgb](image8.png)
<br>
<br>

### ix) Split and merge RGB Image:
![split img](image9.png)
<br>
<br>

### x) Split and merge HSV Image:
![alt text](image10.png)
<br>
<br>




## Result:
Thus the images are read, displayed, written ,and color conversion was performed between RGB, HSV and YCbCr color models is successfully executed using the python program.







