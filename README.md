# Image-Transformation
## Aim:
       To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Import the required libraries and read the original image.

## Step2:
Translate the image.

## Step3:
Scale the image.

## Step4:
Shear the image.

## Step5:
Find reflection of image.

## Step 6:
Rotate the image.

## Step 7:
Crop the image.

## Step 8:
Display all the Transformed images.
## Program:
```
Developed By:S.ABHISHEK
Register Number:212221230002


import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("poohandboy.jfif")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(image)
plt.show()
rows,cols,dim = image.shape
```
## i)Image Translation
```
M = np.float32([[1,0,100],
               [0,1,200],
               [0,0,1]])
translated_image = cv2.warpPerspective(image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()

```


## ii) Image Scaling
```
M = np.float32([[1.5,0,0],
               [0,1.8,0],
               [0,0,1]])
scaled_image = cv2.warpPerspective(image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()
```


## iii)Image shearing
```
M_x = np.float32([[1,0.5,0],
                 [0,1,0],
                 [0,0,1]])
M_y = np.float32([[1,0,0],
                 [0.5,1,0],
                 [0,0,1]])
sheared_xaxis = cv2.warpPerspective(image,M_x,(int(cols*1.5),int(rows*1.5)))
sheared_yaxis = cv2.warpPerspective(image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_yaxis)
plt.show()
```


## iv)Image Reflection
```
M_x = np.float32([[1,0,0],
                 [0,-1,rows],
                 [0,0,1]])
M_y = np.float32([[-1,0,cols],
                 [0,1,0],
                 [0,0,1]])
reflected_xaxis = cv2.warpPerspective(image,M_x,(int(cols),int(rows)))
reflected_yaxis = cv2.warpPerspective(image,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_yaxis)
plt.show()
```



## v)Image Rotation
```
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_image = cv2.warpPerspective(image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_image)
plt.show()
```



## vi)Image Cropping
```
cropped_image = image[100:300,100:300]
plt.axis('off')
plt.imshow(cropped_image)
plt.show()

```

## Output:
## Original image
![image](https://user-images.githubusercontent.com/66360846/232119339-794f8927-c83a-4c12-81d6-b1e3846b2374.png)

## i)Image Translation
![image](https://user-images.githubusercontent.com/66360846/232119386-5773701a-bbab-4b76-a616-61907f71084a.png)

## ii) Image Scaling
![image](https://user-images.githubusercontent.com/66360846/232119742-0b0fb9c5-3489-4498-9de0-3f435e779ef5.png)

## iii)Image shearing
![image](https://user-images.githubusercontent.com/66360846/232119784-172d9446-2e89-4914-b801-627970b3a7b9.png)

## iv)Image Reflection
![image](https://user-images.githubusercontent.com/66360846/232119819-1c7adf90-af14-4f08-93a5-eede248566a2.png)

## v)Image Rotation
![image](https://user-images.githubusercontent.com/66360846/232119857-80904d05-a7af-460f-a924-865bfd13a78a.png)

## vi)Image Cropping
![image](https://user-images.githubusercontent.com/66360846/232119895-75beba22-9ea8-4210-af42-dfc974fd504d.png)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
