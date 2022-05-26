# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
</br> 

### Step2
</br>
</br> 

### Step3
</br>
</br> 

### Step4
</br>
</br> 

### Step5
</br>
</br> 

## Program:
### Developed By   :
### Register Number:
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("flow.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)

kernel1 = np.ones((11,11),np.float32)/121
avg_filter = cv2.filter2D(original_image,-1,kernel1)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(avg_filter)
plt.title("Filtered")
plt.axis("off")



```
ii) Using Weighted Averaging Filter
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("flow.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(weighted_filter)
plt.title("Filtered")
plt.axis("off")




```
iii) Using Gaussian Filter
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("flow.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0, sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Filtered")
plt.axis("off")




```

iv) Using Median Filter
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("flow.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
median = cv2.medianBlur(src=original_image,ksize = 11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Filtered")
plt.axis("off")




```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("flow.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Filtered")
plt.axis("off")




```
ii) Using Laplacian Operator
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("flow.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title("Filtered")
plt.axis("off")




```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
![1](https://user-images.githubusercontent.com/94154679/170519023-32655f18-1a18-475c-afa5-e410b76aaa0b.png)

</br>


ii) Using Weighted Averaging Filter
</br>
![2](https://user-images.githubusercontent.com/94154679/170519089-639c423f-d898-41c0-8874-7733aa562e42.png)

</br>


iii) Using Gaussian Filter
</br>
![3](https://user-images.githubusercontent.com/94154679/170519156-2fc114af-6fdf-45dd-8a56-4ae7ded43163.png)

</br>


iv) Using Median Filter
</br>
![4](https://user-images.githubusercontent.com/94154679/170519189-41d85311-b819-4e92-ac9d-9ca5159a3cbd.png)

</br>


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
![5](https://user-images.githubusercontent.com/94154679/170519228-d0871e62-2001-4966-8c06-80cc95374d5c.png)

</br>


ii) Using Laplacian Operator
</br>
![6](https://user-images.githubusercontent.com/94154679/170519315-b49d2190-c6f1-43d2-969a-46ba011e12e3.png)

</br>


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
