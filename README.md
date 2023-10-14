# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages to do Erosion and Dilution.

### Step2:
Create the text image of our name using putText from cv2 package.

### Step3:
Create the required structural element.

### Step4:
Apply Erode and Dilution for our NameImage.

### Step5:
Display the output images.

### Step6:
End the programm

 
## Program:

```
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,"Adhithya.S",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(image,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
image_erode=cv2.erode(image,kernel)
plt.imshow(image_erode,cmap='gray')
plt.title('Eroded Text'), plt.xticks([]), plt.yticks([])
plt.show()
image_dilate=cv2.dilate(image,kernel)
plt.imshow(image_dilate,cmap='gray')
plt.title('Dilated Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
## Output:

### Display the input Image
![Screenshot 2023-10-14 160635](https://github.com/s-adhithya/EROSION-AND-DILATION/assets/113497423/b6efe1a7-e557-4738-a14c-28a8d00ceb50)

### Display the Eroded Image
![Screenshot 2023-10-14 160647](https://github.com/s-adhithya/EROSION-AND-DILATION/assets/113497423/95925957-85e5-4813-bd2f-2f2fab9eb33e)

### Display the Dilated Image
![Screenshot 2023-10-14 160656](https://github.com/s-adhithya/EROSION-AND-DILATION/assets/113497423/978fd161-36c7-463d-a531-eb9d2c1b3e12)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
