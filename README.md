# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the image using imread()

### Step2:
print the image using imshow()

### Step3:
import numpy for take the pixels in matrix form

### Step4:
import matplotlib.pyplot for showing the image.

### Step5:
By importing the open cv we can change image color.


## Program:
```python
Developed By: D.B.V.SAI GANESH
Register Number: 212223240025
i)Image Translation

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread("tower.jpg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,100],[0,1,200],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
print("Image Translation:")
plt.imshow(translated_image)
plt.show()

ii) Image Scaling

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('tower.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
print("Image Scaling:")
plt.imshow(translated_image)
plt.show()

iii)Image shearing

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('tower.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M2=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols*1.5),int(rows*1.5)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
print("Image Shearing:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()


iv)Image Reflection

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('tower.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()


v)Image Rotation

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('tower.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
print("Image Rotaion:")
plt.imshow(translated_image)
plt.show()


vi)Image Cropping

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('tower.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
print("Image Cropping:")
plt.imshow(translated_image)
plt.show()



```
## Output:
### i)Image Translation
![image](https://github.com/saiganesh2006/IMAGE-TRANSFORMATIONS/assets/145742342/e3245a46-f8d1-4185-a30b-8fdea8078b24)

### ii) Image Scaling

![image](https://github.com/saiganesh2006/IMAGE-TRANSFORMATIONS/assets/145742342/357ef62c-8ac2-4a4d-a4cc-6f00a12d1487)


### iii)Image shearing

![image](https://github.com/saiganesh2006/IMAGE-TRANSFORMATIONS/assets/145742342/d58878b2-18b8-425d-aa7d-815aaba85f96)


### iv)Image Reflection

![image](https://github.com/saiganesh2006/IMAGE-TRANSFORMATIONS/assets/145742342/af2da226-1f81-4fa7-ac5c-07f3773886c7)

### v)Image Rotation

![image](https://github.com/saiganesh2006/IMAGE-TRANSFORMATIONS/assets/145742342/77e88311-51be-46b1-8d5c-d8ad0d2bd5b3)

### vi)Image Cropping

![image](https://github.com/saiganesh2006/IMAGE-TRANSFORMATIONS/assets/145742342/f2b393e2-2fed-410e-bd6b-9c068cef00f2)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
