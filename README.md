# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the required libraries and image for transformation.

### Step2:

Perform operations on the image like translaton, rotation and other.

### Step3:

Use the warpPerspective(image , matrix, (rows, columns)) function.

### Step4:

Plot the Image and Transformed Image on the graph using matplotlib for identifying changes.

### Step5:

Diifferent operations has been performed on the image.


## Program:
~~~
##Developed By: SYED MUHAMMED ZAHI
##Register Number: 212221230114

##i)Image Translation

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread ("car.jpeg")
input_image = cv2. cvtColor (input_image, cv2. COLOR_BGR2RGB)
plt. axis('off')
plt.imshow(input_image)
plt. show()
rows, cols, dim = input_image.shape
M = np. float32([[1, 0, 300],[0, 1, 300],[0, 0, 1]])
translated_image = cv2.warpPerspective (input_image, M, (cols, rows))
plt.axis("off")
plt.imshow(translated_image)
plt.show()


##ii) Image Scaling

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("car.jpeg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

##iii)Image shearing

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("car.jpeg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()


##iv)Image Reflection

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("car.jpeg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()


##v)Image Rotation

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("car.jpeg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

##vi)Image Cropping

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("car.jpeg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
~~~

## OUTPUT:
### ORIGINAL IMAGE:
![image](https://github.com/SdMdZahi7/IMAGE-TRANSFORMATIONS/assets/94187572/ac992848-880d-4e37-9c89-1e6e47c22167)
### 1)IMAGE TRANSLATION:
![image](https://github.com/SdMdZahi7/IMAGE-TRANSFORMATIONS/assets/94187572/42476d20-d524-4108-8014-f268f590ec61)
### 2)IMAGE SCALING:
![image](https://github.com/SdMdZahi7/IMAGE-TRANSFORMATIONS/assets/94187572/919e1df0-8d08-46ae-b30d-81e297911cdd)
### 3)IMAGE SHEARING:
![image](https://github.com/SdMdZahi7/IMAGE-TRANSFORMATIONS/assets/94187572/cb3adb41-87ae-4d72-8d0a-b22f09745850)
![image](https://github.com/SdMdZahi7/IMAGE-TRANSFORMATIONS/assets/94187572/947980a0-3019-4f8d-8391-57d655be5f7e)





## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
