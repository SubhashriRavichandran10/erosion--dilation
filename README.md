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


import cv2
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline

def load_img():
    blank_img = np.zeros((600, 600), dtype='uint8')
    font = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img, text='ABCDE', org=(50, 300), fontFace=font,
                fontScale=5, color=(255, 255, 255), thickness=25, lineType=cv2.LINE_AA)
    return blank_img

def display_img(img):
    plt.figure(figsize=(12,10))
    plt.imshow(img, cmap='gray')
    plt.axis('off')
    plt.show()

# Load image
img = load_img()
display_img(img)

# ✅ Define the kernel before using it
kernel = np.ones((5,5), np.uint8)

# Apply erosion
eroded = cv2.erode(img, kernel, iterations=2)
display_img(eroded)

# Apply dilation
dilated = cv2.dilate(img, kernel, iterations=2)
display_img(dilated)









```

## Output:

### Display the input Image

<img width="682" height="659" alt="image" src="https://github.com/user-attachments/assets/64d26b3c-9d42-4a25-9f82-e3d7a06eb5f5" />


### Display the Eroded Image

<img width="758" height="656" alt="image" src="https://github.com/user-attachments/assets/ee601da9-5ea1-4204-a026-fcb66dc44b8b" />


### Display the Dilated Image


<img width="712" height="648" alt="image" src="https://github.com/user-attachments/assets/04945d58-2092-4545-b388-52b479892111" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
