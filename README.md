# IMAGE TRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.

### Step2:
Load the image file in the program.

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4
Display the modified image output.

### Step5:
End the program.



## Program:
```
Developed By: MUKESH V
Register Number: 212222230086
```
i)Image Translation
``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("Elephant.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(in_img)
plt.show()
```
ii) Image Scaling
``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("Elephant.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1,0,50],
              [0,1,50],
              [0,0,1]])
trans_img=cv2.warpPerspective(in_img, M, (cols,rows))
plt.axis('off')
plt.imshow(trans_img)
plt.show() 
```
iii)Image shearing
``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("Elephant.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()
```
iv)Image Reflection
``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("Elephant.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  
```
v)Image Rotation
``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("Elephant.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()  
```
vi)Image Cropping
``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("Elephant.jpg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[10:150 ,10:250]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation
![Screenshot 2023-09-13 233749](https://github.com/MukeshVelmurugan/IMAGETRANSFORMATION/assets/118707363/d4428963-6900-411d-a121-b983c211f0cc)
### ii) Image Scaling
![Screenshot 2023-09-13 233837](https://github.com/MukeshVelmurugan/IMAGETRANSFORMATION/assets/118707363/9b729042-0c67-4161-ad9a-518a7a6c84ef)


### iii)Image shearing
![Screenshot 2023-09-13 233933](https://github.com/MukeshVelmurugan/IMAGETRANSFORMATION/assets/118707363/9f863544-ef94-42f8-80e8-64bb0870aebf)

![Screenshot 2023-09-13 233944](https://github.com/MukeshVelmurugan/IMAGETRANSFORMATION/assets/118707363/ec497d90-65b3-4fc7-a375-f74c20e75b6b)


### iv)Image Reflection
![Screenshot 2023-09-13 234128](https://github.com/MukeshVelmurugan/IMAGETRANSFORMATION/assets/118707363/c0dba7d1-e3e2-43e9-b759-33d072cace14)
![Screenshot 2023-09-13 234135](https://github.com/MukeshVelmurugan/IMAGETRANSFORMATION/assets/118707363/be2cb98e-5bcb-42d6-91b8-bddf284d5cd7)


### v)Image Rotation
![Screenshot 2023-09-13 234234](https://github.com/MukeshVelmurugan/IMAGETRANSFORMATION/assets/118707363/95879fd6-431e-4aa1-b71d-7d22bcf4fb72)


### vi)Image Cropping

#### Original
![Screenshot 2023-09-13 234602](https://github.com/MukeshVelmurugan/IMAGETRANSFORMATION/assets/118707363/70ada784-f449-4f00-9705-bd0091133ccb)

#### Cropped

![image](https://github.com/MukeshVelmurugan/IMAGETRANSFORMATION/assets/118707363/30449a63-b6f2-437b-9fdf-d17e6695f1b7)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
