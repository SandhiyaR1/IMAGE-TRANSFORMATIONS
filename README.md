# IMAGE-TRANSFORMATIONS


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

### Step4:
Display the modified image output.

### Step5:
End the program.


## Program:
```
Developed By:SANDHIYA R
Register Number:212222230129
```
### i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread( "lotus.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis( 'off')
plt.imshow(input_image)
plt.show()
rows,cols,dim =input_image.shape
M =np.float32([[1,0,100],
               [0,1,100],
               [0,0,1]])
translated_image =cv2.warpPerspective(input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
### ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("lotus.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1.5,0 ,0],
              [0,1.8,0],
              [0,0,1]])
scaled_img=cv2.warpPerspective(in_img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```

### iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("lotus.jpg")
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
### iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("lotus.jpg")
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
### v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("lotus.jpg")
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
### vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("lotus.jpg")
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
![download](https://github.com/SandhiyaR1/IMAGE-TRANSFORMATIONS/assets/113497571/bf95d6a5-77c0-41a8-a0fb-3972d376d147)

![download](https://github.com/SandhiyaR1/IMAGE-TRANSFORMATIONS/assets/113497571/273e39a8-681a-4e83-835e-1cd7432dd024)


### ii) Image Scaling

![download](https://github.com/SandhiyaR1/IMAGE-TRANSFORMATIONS/assets/113497571/a9f6ee0a-3b2c-4ff2-a667-d9a9c8130fd6)


### iii)Image shearing
![download](https://github.com/SandhiyaR1/IMAGE-TRANSFORMATIONS/assets/113497571/8ac8d39c-673f-4fa6-aec9-7d61148543fd)

![download](https://github.com/SandhiyaR1/IMAGE-TRANSFORMATIONS/assets/113497571/8d7fd57f-9867-4b76-aafd-b3cc28fc8557)

### iv)Image Reflection

![download](https://github.com/SandhiyaR1/IMAGE-TRANSFORMATIONS/assets/113497571/1d3f94b7-ec07-44ba-9c25-e6f92dd64bb9)

![download](https://github.com/SandhiyaR1/IMAGE-TRANSFORMATIONS/assets/113497571/45838512-2213-41f5-a69c-49b860cde965)




### v)Image Rotation

![download](https://github.com/SandhiyaR1/IMAGE-TRANSFORMATIONS/assets/113497571/9b331ee6-c70a-4fd3-bc29-7e9171cddfcc)



### vi)Image Cropping

![download](https://github.com/SandhiyaR1/IMAGE-TRANSFORMATIONS/assets/113497571/810467f5-c4a8-4cd8-815b-ff04d62b30e8)

![download](https://github.com/SandhiyaR1/IMAGE-TRANSFORMATIONS/assets/113497571/b05a885d-2f2c-4dc4-ba22-ba8106473539)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
