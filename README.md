# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
<br>Translate the image using a function warpPerpective()

### Step3:
<br>Scale the image by multiplying the rows and columns with a float value.

### Step4:
<br>Shear the image in both the rows and columns.

### Step5:
<br>Find the reflection of the image.

### Step6:
<br>Rotate the image using angle function.

## Program:
```python
Developed By: M.JAYACHANDRAN
Register Number: 212222240038
```

i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("dip4.jpg")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```


ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dip4.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```


iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dip4.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```


iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dip4.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```



v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dip4.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```



vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("dip4.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()
```

## Output:
### i)Image Translation

![1](https://github.com/Jayachandran20/IMAGE-TRANSFORMATIONS/assets/118447015/4afddb82-f11d-4d62-b92c-56a152b041db)

### ii) Image Scaling
![scaling](https://github.com/Jayachandran20/IMAGE-TRANSFORMATIONS/assets/118447015/a710bc4d-34b8-456a-8342-15e6fcfdadd9)


### iii)Image shearing

![shearing](https://github.com/Jayachandran20/IMAGE-TRANSFORMATIONS/assets/118447015/c0eb0d87-2137-4ffd-90ec-19e1d711b6d1)

### iv)Image Reflection

![reflection](https://github.com/Jayachandran20/IMAGE-TRANSFORMATIONS/assets/118447015/14b078d2-a95f-4237-bf2b-4d992cb4f9c4)

### v)Image Rotation

![rotation](https://github.com/Jayachandran20/IMAGE-TRANSFORMATIONS/assets/118447015/c1333aca-e2af-4119-bde6-0e76f2e9f88e)

### vi)Image Cropping

![croppping](https://github.com/Jayachandran20/IMAGE-TRANSFORMATIONS/assets/118447015/c46929aa-e8f8-449e-b2ec-d0b7be0b154b)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
