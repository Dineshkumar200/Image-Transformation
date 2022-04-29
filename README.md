# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the necessary libraries and read the original image and save it a image variable.
### Step2:

Translate the image using Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]]) Translated_image=cv2.warpPerspective(org_img,Translation_matrix,(col,row))
### Step3:
Scale the image using 
Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]]) Scaled_image=cv2.warpPerspective(org_img,Scaling_Matrix,(col,row))

### Step4:
Shear the image using 

Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]]) Sheared_image=cv2.warpPerspective(org_img,Shearing_matrix,(col2,int(row1.5)))

### Step5:
Reflection of image can be achieved through the code Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]]) Reflected_image_row=cv2.warpPerspective(org_img,Reflection_matrix_row,(col,int(row)))
### Step6:
Rotate the image using Rotation_angle=np.radians(10) Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0], [np.sin(Rotation_angle),np.cos(Rotation_angle),0], [0,0,1]]) Rotated_image=cv2.warpPerspective(org_img,Rotation_matrix,(col,(row)))
### Step7:
Crop the image using cropped_image=org_img[10:350,320:560]
### Step8:
Display all the Transformed images.
## Program:
```python
Developed By: Dineshkumar V
Register Number:212220230013  





```
## Output:
### i)Image Translation

![e2](https://user-images.githubusercontent.com/75235789/165889308-77dce921-2fea-4e92-8fe7-2bba7b7ab0df.jpg)


### ii) Image Scaling

![e3](https://user-images.githubusercontent.com/75235789/165889311-10d83f42-c582-41e8-b3d3-436b60566774.jpg)


### iii)Image shearing

![e4](https://user-images.githubusercontent.com/75235789/165889317-9c540ba6-b406-4339-849e-11a658bb0d1b.jpg)

### iv)Image Reflection

![e5](https://user-images.githubusercontent.com/75235789/165889320-db2d9f0f-8aee-413f-bbe1-70815d12c960.jpg)


### v)Image Rotation

![e6](https://user-images.githubusercontent.com/75235789/165889325-80f89043-35f6-4039-b18d-8b82855c2a72.jpg)




### vi)Image Cropping

![e7](https://user-images.githubusercontent.com/75235789/165889340-0c8abe2b-7d93-46e8-8370-ade488dbe3bb.jpg)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
