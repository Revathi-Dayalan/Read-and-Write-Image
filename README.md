# READ AND WRITE AN IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.
i) Read, display, and write an image.
ii) Access the rows and columns in an image.
iii) Cut and paste a small portion of the image.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
## Program:
### Developed By:
### Register Number: 
i) #To Read,display the image
```python
import cv2
dog_image = cv2.imread('dog.jpg',1)
cv2.imshow('Puppy',dog_image)
cv2.waitKey(0)
destroyAllWindows()
```
ii) #To write the image
```python
cv2.imwrite('new1.jpg',dog_image)
```
iii) #Find the shape of the Image
```python3
import cv2
dog_image = cv2.imread('dog.jpg',1)
print(dog_image.shape)
```
iv) #To access rows and columns

```python3
import random
for i in range(100):
    for j in range(dog_image.shape[1]):
        dog_image[i][j] = [random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2.imshow('Dog',dog_image)
cv2.waitKey(0)
destroyAllWindows()

```
v) #To cut and paste portion of image
```python3
import cv2
dog_image = cv2.imread('dog.jpg',-1)
tag = dog_image[300:400,300:400]
dog_image[50:150,50:150] = tag
cv2.imshow('Dog',dog_image)
cv2.waitKey(0)
destroyAllWindows()
```

## Output:

### i) Read and display the image
![o1](https://user-images.githubusercontent.com/96000574/166143384-5a79faa9-0473-4773-9e50-c5526c27fe75.PNG)
<br>
<br>

### ii)Write the image
![o2](https://user-images.githubusercontent.com/96000574/166143396-8599a420-f93c-4638-8b5f-5deeb1e28fe2.PNG)
<br>
<br>

### iii)Shape of the Image
![o3](https://user-images.githubusercontent.com/96000574/166143405-9ec50070-d9d8-40eb-9588-3638562cc164.PNG)

<br>
<br>

### iv)Access rows and columns

![o4](https://user-images.githubusercontent.com/96000574/166143420-08beb76f-c9de-459c-928f-66e8ab134110.PNG)

<br>
<br>

### v)Cut and paste portion of image

![o5](https://user-images.githubusercontent.com/96000574/166143425-d834cbad-124b-4bb9-abff-173ce25c8070.PNG)

<br>
<br>

## Result:
Thus the images are read, displayed, and written successfully using the python program.


