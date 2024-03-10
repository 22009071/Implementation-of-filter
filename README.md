# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.


### Step2
Convert the image from BGR to RGB.


### Step3
Apply the required filters for the image separately.


### Step4
Plot the original and filtered image by using matplotlib.pyplot.


### Step5
End the program.


## Program:
### Developed By   : kabilan T
### Register Number: 212222230059

</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```python
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("wp6959765-jackie-chan-adventures-wallpapers.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()




```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()









```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()




```

iv) Using Median Filter
```Python

median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()








```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()








```
ii) Using Laplacian Operator
```Python


laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()








```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>![image](https://github.com/22009071/Implementation-of-filter/assets/120206067/fb7b15a3-b4dc-4334-a3dc-265c9872c310)

</br>
</br>
</br>
</br>

ii) Using Weighted Averaging Filter
</br>![image](https://github.com/22009071/Implementation-of-filter/assets/120206067/182d59b8-ce7a-4335-942b-2533329a00b3)

</br>
</br>
</br>
</br>

iii) Using Gaussian Filter
</br>![image](https://github.com/22009071/Implementation-of-filter/assets/120206067/668321e5-c346-4ede-bd89-f884f387a8de)

</br>
</br>
</br>
</br>

iv) Using Median Filter
</br>![image](https://github.com/22009071/Implementation-of-filter/assets/120206067/521f1cab-9862-45a6-851b-3228051fbf9d)

</br>
</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>![image](https://github.com/22009071/Implementation-of-filter/assets/120206067/daf58f67-eff2-49bc-8d95-f5e807de81fa)

</br>
</br>
</br>
</br>

ii) Using Laplacian Operator
</br>![image](https://github.com/22009071/Implementation-of-filter/assets/120206067/c3b85813-cfa0-46af-b89f-91ae75d44d56)

</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
