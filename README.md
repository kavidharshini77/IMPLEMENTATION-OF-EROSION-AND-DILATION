# IMPLEMENTATION-OF-EROSION-AND-DILATION
# Name : KAVIDHARSHINI RAMESH
# Reg No : 212225240069
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>
Import the necessary pacakages

### Step2:
<br>
Create the text using cv2.putText

### Step3:
<br>
Create the structuring element

### Step4:
<br>
Erode the image

### Step5:
<br>
Dilate the Image
 
## Program:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'KAVIDHARSHINI RAMESH', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
array([[[0, 0, 0],
        [0, 0, 0],
        [0, 0, 0],
        ...,
        [0, 0, 0],
        [0, 0, 0],
        [0, 0, 0]],

       [[0, 0, 0],
        [0, 0, 0],
        [0, 0, 0],
        ...,
        [0, 0, 0],
        [0, 0, 0],
        [0, 0, 0]],

       [[0, 0, 0],
        [0, 0, 0],
        [0, 0, 0],
        ...,
        [0, 0, 0],
        [0, 0, 0],
        [0, 0, 0]],

       ...,
...
        [0, 0, 0],
        ...,
        [0, 0, 0],
        [0, 0, 0],
        [0, 0, 0]]], shape=(500, 500, 3), dtype=uint8)
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)
# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)
# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')


```
## Output:
<img width="782" height="585" alt="image" src="https://github.com/user-attachments/assets/cecd7319-f3a5-4dec-8b10-78924593a476" />

<img width="777" height="590" alt="image" src="https://github.com/user-attachments/assets/70c25561-4ef0-4f23-b599-0ea18b5cd7ce" />

<img width="796" height="597" alt="image" src="https://github.com/user-attachments/assets/35e07db6-71cc-4d2b-9f5b-dfc05525406d" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
