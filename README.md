# Basics-of-Image-Transformations-Using-OpenCV

# Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

# Software Required:
Anaconda - Python 3.7

# Algorithm:
### Step1:
Read the color image using imread().
### Step2:
Print the image using imshow().
### Step3:
Perform Translation, Scaling, Shearing on the image.
### Step4:
And perform Reflection, Rotation, Cropping on the image.
### Step5:
Display the output.
# Program:

**Developed By: Gnanendran N  
Register Number: 212223240037**

```python
i)Image Translation

tx, ty = 100, 50
M_translation = np.float32([[1, 0, tx], [0, 1, ty]])

translated_image = cv2.warpAffine(image, M_translation, (2500, 1400))

ii) Image Scaling

fx, fy = 2.5, 2.0  
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)

iii)Image shearing

shear_matrix = np.float32([[1, 0.3, 0], [0.3, 1, 0]])  
sheared_image = cv2.warpAffine(image, shear_matrix, (2800, 2100))

iv)Image Reflection

reflected_image = cv2.flip(image, 2)

v)Image Rotation

(height, width) = image.shape[:2] 
angle = 35 
center = (width // 2, height // 2)
M_rotation = cv2.getRotationMatrix2D(center, angle, 1)

rotated_image = cv2.warpAffine(image, M_rotation, (width, height)) 

vi)Image Cropping

x, y, w, h = 800, 300, 900, 700  
cropped_image = image[y:y+h, x:x+w]
```
# Output:
### i)Image Translation
<img width="912" height="387" alt="image" src="https://github.com/user-attachments/assets/d341aea3-e7ee-4a8f-a4e0-0f9f52e6473f" />

### ii) Image Scaling
<img width="837" height="322" alt="image" src="https://github.com/user-attachments/assets/0918eb03-735e-418c-b8c4-373e1d4cbfb1" />

### iii)Image shearing
<img width="817" height="490" alt="image" src="https://github.com/user-attachments/assets/6d1468cc-dfb0-412b-94ce-4ef8d2d2b246" />

### iv)Image Reflection
<img width="1238" height="374" alt="image" src="https://github.com/user-attachments/assets/75149d64-4f24-495e-b7f9-6c2266e3930a" />

### v)Image Rotation
<img width="795" height="353" alt="image" src="https://github.com/user-attachments/assets/cd0dcc30-354c-4b8f-a4f9-be81e9c85014" />

### vi)Image Cropping
<img width="965" height="544" alt="image" src="https://github.com/user-attachments/assets/84527377-9aaf-4ee7-9015-ed04aaca7ca6" />


# Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
