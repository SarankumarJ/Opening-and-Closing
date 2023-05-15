# Opening-and-Closing
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
Anaconda - Python 3.7
OpenCV
## Algorithm:-
### Step1:
Import the necessary packages cv2, numpy and matplotlib.

### Step2:
Create the text using the built in function cv2.putText()

### Step3:
Create the structuring element.

### Step4:
Perform opening and closing using the function cv2.MORPH_OPEN and cv2.MORPH_CLOSE

### Step5:
Run the programs and execute the outputs.


## Program:
#### Program developed by : Sarankumar J
#### Register number : 212221230087
```py
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image=np.zeros((100,300), dtype = 'uint8')
font=cv2.FONT_HERSHEY_COMPLEX
cv2.putText(image,'BALA_07',(5,70), font, 2,(255),5,cv2.LINE_AA)
plt.imshow(image)
plt.axis('off')
plt.title('Original image')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
open1 = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
plt.imshow(open1)
plt.axis('off')
plt.title('Opening')

# Use Closing Operation
close1 = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(close1)
plt.axis('off')
plt.title('Closing')
```
## Output:
### Display the input Image
![image](https://github.com/SarankumarJ/Opening-and-Closing/assets/94778101/a179bd06-635d-4f5b-a378-24636cdeac34)

### Display the result of Opening
![opening](https://github.com/SarankumarJ/Opening-and-Closing/assets/94778101/390e0aea-92af-455b-afcc-7906eed10b22)

### Display the result of Closing
![closing](https://github.com/SarankumarJ/Opening-and-Closing/assets/94778101/50aedff9-2e22-446c-b65b-0dacc3abba4a)

## Result:-
Thus the Opening and Closing operation is used in the image using python and OpenCV.
