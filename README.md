# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Create a blank image.

### Step2:

Create a structuring element (5x5 rectangular)

### Step3:

Erode the image.

### Step4:
Dilate the image.

### Step5:


 End the program.
## Program:


```

# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline

# Create the Text using cv2.putText

def load_img():
    blank_img =np.zeros((600,600))
    font = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img,text='ABCDE',org=(50,300), fontFace=font,fontScale= 5,color=(255,255,255),thickness=25,lineType=cv2.LINE_AA)
    return blank_img

# Create the structuring element

def display_img(img):
    fig = plt.figure(figsize=(12,10))
    ax = fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    plt.show()

# Erode the image
erosion1 = cv2.erode(img,kernel,iterations = 2)
display_img(erosion1)



# Dilate the image
dilated_img = cv2.dilate(img,kernel,iterations = 2)
display_img(dilated_img)









`
```

## Output:

### Display the input Image



### Display the Eroded Image


### Display the Dilated Image


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
