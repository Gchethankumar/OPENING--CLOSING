# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

## Program:
```
Developed by: Chethan Kumar G
Register No: 212222240022
```

### Import the necessary packages
``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### Create the Text using cv2.putText
```python
img=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'Chethan Kumar G',(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Original Image",img)
```

### Create the structuring element
```python
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))
```

### Use Opening operation
```pytohn
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
cv2.imshow("Opening image",image_open)
```

### Use Closing Operation
```python
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
cv2.imshow("Closing Image",image_close)
```
## Output:

### Display the input Image

![Screenshot from 2023-10-11 16-16-29](https://github.com/Gchethankumar/OPENING--CLOSING/assets/118348224/0c0af412-9387-4277-b4b5-8aafc0746e03)


### Display the result of Opening

![Screenshot from 2023-10-11 16-16-35](https://github.com/Gchethankumar/OPENING--CLOSING/assets/118348224/0bc1736d-4991-4c80-b95f-210a224a4c9c)


### Display the result of Closing

![Screenshot from 2023-10-11 16-16-41](https://github.com/Gchethankumar/OPENING--CLOSING/assets/118348224/88ecf8cc-64bd-4060-8161-cccfa29be26d)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
