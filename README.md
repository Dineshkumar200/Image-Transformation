# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it a image variable.
### Step2:
Translate the image using Translation_matrix.
### Step3:
Scale the image using Scaling_Matrix.
### Step4:
Shear the image using Shearing_matrix.
### Step5:
Reflection of image can be achieved through the code Reflection_matrix_row.
### Step6:
Rotate the image using Rotation_angle=np.radians(10) Rotation_matrix
### Step7:
Crop the image using cropped_image.
### Step8:
Display all the Transformed images.
## Program:
```python
Developed By: Dineshkumar V
Register Number:212220230013  


import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("jk.jpg")
img= cv2.cvtColor (img, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(img)
plt.show()

i)Image Translation

shape=img.shape
rows, cols, dim = shape

M=np.float32([[1,0,80],
          [0,1,75],
          [0,0,1]])
translated_img=cv2.warpPerspective(img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()

ii) Image Scaling

rows, cols, dim = shape
M = np.float32 ([[1.5, 0, 0],
[0, 1.8, 0],
[0, 0, 1]])

scaled_img = cv2.warpPerspective (img, M, (cols*2, rows*2))
plt.axis ('off')

plt.imshow (scaled_img)
plt.show()



iii)Image Shearing


Mx=np.float32([[1,0.5,0],
          [0,1,75],
          [0,0,1]])
My=np.float32([[1,0,0],
              [0.5,1,0],
               [0,0,1]])
shx_img=cv2.warpPerspective(img,Mx,(int(cols),int(rows)))
shy_img=cv2.warpPerspective(img,My,(int(cols),int(rows)))
plt.axis ('off')

plt.imshow (shx_img)
plt.show()
plt.axis ('off')
plt.imshow (shy_img)
plt.show()


iv)Image Reflection

Mx=np.float32([[1,0,0],
          [0,-1,rows],
          [0,0,1]])
My=np.float32([[-1,0,cols],
              [0,1,0],
               [0,0,1]])
refx_img=cv2.warpPerspective(img,Mx,(int(cols),int(rows)))
refy_img=cv2.warpPerspective(img,My,(int(cols),int(rows)))
plt.axis ('off')

plt.imshow (refx_img)
plt.show()
plt.axis ('off')
plt.imshow (refy_img)
plt.show()


v)Image Rotation

angle=np.radians(27)
Rotation_matrix=np.float32([[np.cos(angle),-np.sin(angle),0],
                                [np.sin(angle),np.cos(angle),0],
                                [0,0,1]])
rotimg=cv2.warpPerspective(img,Rotation_matrix,(int(cols),int(rows)))
plt.axis ('off')

plt.imshow (rotimg)
plt.show()



vi)Image Cropping

cropimg=img[60:400,60:400]
plt.axis ('off')

plt.imshow (cropimg)
plt.show()




```
## Output:
### i)Image Translation

![e2](https://user-images.githubusercontent.com/75235789/165889308-77dce921-2fea-4e92-8fe7-2bba7b7ab0df.jpg)


### ii) Image Scaling

![e3](https://user-images.githubusercontent.com/75235789/165889311-10d83f42-c582-41e8-b3d3-436b60566774.jpg)


### <br/><br/><br/><br/><br/><br/><br/><br/><br/>iii)Image shearing

<br/>![e4](https://user-images.githubusercontent.com/75235789/165889317-9c540ba6-b406-4339-849e-11a658bb0d1b.jpg)

### <br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>iv)Image Reflection

![e5](https://user-images.githubusercontent.com/75235789/165889320-db2d9f0f-8aee-413f-bbe1-70815d12c960.jpg)


### v)Image Rotation

![e6](https://user-images.githubusercontent.com/75235789/165889325-80f89043-35f6-4039-b18d-8b82855c2a72.jpg)




### <br/><br/><br/><br/><br/><br/><br/><br/>vi)Image Cropping

![e7](https://user-images.githubusercontent.com/75235789/165889340-0c8abe2b-7d93-46e8-8370-ade488dbe3bb.jpg)



## <br/><br/><br/><br/><br/><br/><br/><br/>Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
