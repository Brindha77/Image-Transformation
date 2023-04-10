# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Import the necessary libraries and read the original image and save it a image variable.

## Step2:
Translate the image using Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]]) Translated_image=cv2.warpPerspective(org_img,Translation_matrix,(col,row))

## Step3:
Scale the image using Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]]) Scaled_image=cv2.warpPerspective(org_img,Scaling_Matrix,(col,row))

## Step4:
Shear the image using Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]]) Sheared_image=cv2.warpPerspective(org_img,Shearing_matrix,(col2,int(row1.5)))

## Step5:
Reflection of image can be achieved through the code Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]]) Reflected_image_row=cv2.warpPerspective(org_img,Reflection_matrix_row,(col,int(row)))

## Step6:
Rotate the image using Rotation_angle=np.radians(10) Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0], [np.sin(Rotation_angle),np.cos(Rotation_angle),0], [0,0,1]]) Rotated_image=cv2.warpPerspective(org_img,Rotation_matrix,(col,(row)))

## Step7:
Crop the image using cropped_image=org_img[10:350,320:560]

## Step8:
Display all the Transformed images.

## Program:
Developed By:R.Brindha
Register Number:21222222230023

i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("maple.jpeg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M= np.float32([[1, 0, 100],
                [0, 1, 200],
                 [0, 0, 1]])
translated_image =cv2.warpPerspective (input_image, M, (cols, rows))
plt.imshow(translated_image)
plt.show()
```

ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("maple.jpeg") 
cv2.imshow
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M = np. float32 ([[1.5, 0 ,0],
                 [0, 2.0 , 0],
                  [0, 0, 2]])
scaled_img=cv2.warpPerspective(input_image, M, (cols*2, rows*2))
plt.imshow(scaled_img)
plt.show()
```

iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("maple.jpeg") 
cv2.imshow
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M = np. float32 ([[1.5, 0 ,0],
                 [0, 2.0 , 0],
                  [0, 0, 2]])
scaled_img=cv2.warpPerspective(input_image, M, (cols*2, rows*2))
plt.imshow(scaled_img)
plt.show()
```

iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("maple.jpeg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.imshow(reflected_img_yaxis)
plt.show()
```


v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("maple.jpeg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```


vi)Image Cropping
```python
cropped_image = input_image[50:100,50:100]
plt.axis('off')
plt.imshow(cropped_image)
plt.show()
```
## Output:
### i)Image Translation
![1](https://user-images.githubusercontent.com/118889143/230828717-d6668058-cef3-4e23-bd1d-e422a7fbf974.png)

### ii) Image Scaling
![2](https://user-images.githubusercontent.com/118889143/230828770-739f59da-1e69-431f-8cee-aac9808abb7b.png)

### iii)Image shearing
![3](https://user-images.githubusercontent.com/118889143/230828835-6238debc-fc72-4e87-8a21-5dc821cfd946.png)

### iv)Image Reflection
![4](https://user-images.githubusercontent.com/118889143/230828860-a979e809-6631-4c96-8e32-ed384f874c65.png)

### v)Image Rotation
![5](https://user-images.githubusercontent.com/118889143/230828914-131c593e-2bc8-4c64-82e3-420896cbce4c.png)

### vi)Image Cropping
![6](https://user-images.githubusercontent.com/118889143/230828940-42e48004-0c2b-4438-b544-a2a6b566cde2.png)

## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
