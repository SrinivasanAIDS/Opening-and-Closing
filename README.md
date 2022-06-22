### Ex No: 11
### Date:

#  <p align="center"> Opening-and-Closing </p>

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.
<br>

### Step2:
Create the text image using cv2.putText.
<br>

### Step3:
Then create the structuring element for opening and closing.
<br>

### Step4:
Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.
<br>

### Step5:
Plot the images using plt.imshow.
<br>

 
## Program:

``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"Srinivasan S",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')


# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))



# Use Opening operation

image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')

# Use Closing Operation

image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')

```
## Output:

### Display the input Image
![image](https://user-images.githubusercontent.com/103049243/171182011-afcc1b88-c633-4985-aae9-387e359b4213.png)

### Display the result of Opening
![image](https://user-images.githubusercontent.com/103049243/171181923-ba22b580-927a-4809-b0be-fb4d54a9a785.png)

### Display the result of Closing
![image](https://user-images.githubusercontent.com/103049243/171181825-5b29e158-fcaa-4d8f-8ee2-4dac7de605e6.png)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
