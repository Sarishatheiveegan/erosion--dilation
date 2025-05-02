# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

### DEVELOPED BY:MARINO SARISHA T
### REG NO:212223240084

## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline


# Create the Text using cv2.putText
def load_img():
    blank_img =np.zeros((600,600))
    font = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img,text='SARIS',org=(50,300), fontFace=font,fontScale= 5,color=(255,255,255),thickness=25,lineType=cv2.LINE_AA)
    return blank_img


# Create the structuring element
def display_img(img):
    fig = plt.figure(figsize=(12,10))
    ax = fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    plt.show()
img = load_img()
display_img(img)
kernel = np.ones((5, 5), dtype=np.uint8)
kernel

# Erode the image
erosion1 = cv2.erode(img,kernel)
display_img(erosion1)


# Dilate the image
dilation = cv2.dilate(img,kernel)
display_img(dilation)



```
## Output:

### Display the input Image
![Screenshot 2025-05-02 114541](https://github.com/user-attachments/assets/d00a9351-176e-48d9-b044-a342513a9470)


### Display the Eroded Image
![Screenshot 2025-05-02 114556](https://github.com/user-attachments/assets/e8d65633-9f85-43bc-86fa-25e51893d2d8)


### Display the Dilated Image
![Screenshot 2025-05-02 114611](https://github.com/user-attachments/assets/b5afa68b-3967-44eb-a7bd-3a8cf0466b41)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
