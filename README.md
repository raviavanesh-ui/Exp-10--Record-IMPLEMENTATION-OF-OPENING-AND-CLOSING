# Exp-10--Record-IMPLEMENTATION-OF-OPENING-AND-CLOSING

## Aim
To implement Opening and Closing using Python and OpenCV.

## developed by
Name:Avanesh.R
reg no:212225240018

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program:

```

import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hello Java', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(cv2.cvtColor(closed_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing  Operation")
plt.axis('off')
```
## Output:

<img width="389" height="410" alt="d0ebd048-f690-492e-93b0-47d3520b4b06" src="https://github.com/user-attachments/assets/6451ad95-25a6-4e8a-9ac4-3e71654ec8b8" />
<img width="389" height="410" alt="82160b1b-dca3-4919-ba9b-a380b6c858a3" src="https://github.com/user-attachments/assets/1d908f4b-7efe-4a45-be30-28ddc57289c9" />
<img width="389" height="410" alt="2bf7fd40-c208-43eb-bf00-dea2a7ed8351" src="https://github.com/user-attachments/assets/d5cba00f-1794-424c-96e9-315256957c53" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
