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
cv2.putText(image, 'MAHALAKSHMI', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
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
<img width="1427" height="1102" alt="ChatGPT Image Sep 7, 2026, 07_09_42 PM" src="https://github.com/user-attachments/assets/1b38e4e7-b753-44fa-9eed-8ebad51c4254" />

<img width="1437" height="1094" alt="ChatGPT Image Sep 7, 2026, 07_11_48 PM" src="https://github.com/user-attachments/assets/65968b31-8619-4f3c-94d3-5c0bb6deb636" />

<img width="1428" height="1102" alt="ChatGPT Image Sep 7, 2026, 07_13_09 PM" src="https://github.com/user-attachments/assets/99cc5f90-19a7-49cf-96ff-58b330d736e4" />

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
